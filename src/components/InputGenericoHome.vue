<template>
    <q-card class="my-card">
        <div class="q-pa-md">
            <q-card-section style="padding: 0">
                <div class="text-p q-mb-xs">{{ Header }}</div>
            </q-card-section>

            <div class="q-gutter-y-md column">
                <q-input v-model="inputModel" filled clearable color="dark" :label="Label" :hint="Hint" :shadow-text="inputShadowText" @keydown="processInputFill" @focus="processInputFill">
                    <template v-slot:append>
                        <img src="../assets/MyLocation.png" />
                    </template>
                </q-input>
            </div>
        </div>
    </q-card>
</template>

<script>
import { event } from "quasar";
import { ref, computed } from "vue";

const { stopAndPrevent } = event;

export default {
    props: {
        Header: String,
        Hint: String,
        Label: String,
    },
    computed: {
        showHeader: function () {
            return this.Header;
        },
        showHint: function () {
            return this.Hint;
        },

        showLabel: function () {
            return this.Label;
        },
    },
    setup() {
        const inputModel = ref("");
        const inputFillCancelled = ref(false);
        const inputShadowText = computed(() => {
            if (inputFillCancelled.value === true) {
                return "";
            }

            const t = "Write here";
            const empty = typeof inputModel.value !== "string" || inputModel.value.length === 0;

            if (empty === true) {
                return t;
            } else if (t.indexOf(inputModel.value) !== 0) {
                return "";
            }

            return t.split(inputModel.value).slice(1).join(inputModel.value);
        });

        const textareaModel = ref("");
        const textareaFillCancelled = ref(false);
        const textareaShadowText = computed(() => {
            if (textareaFillCancelled.value === true) {
                return "";
            }

            const t = "This text\nwill be filled\non multiple lines\nwhen you press TAB",
                empty = typeof textareaModel.value !== "string" || textareaModel.value.length === 0;

            if (empty === true) {
                return t.split("\n")[0];
            } else if (t.indexOf(textareaModel.value) !== 0) {
                return "";
            }

            return t.split(textareaModel.value).slice(1).join(textareaModel.value).split("\n")[0];
        });

        return {
            inputModel,
            inputFillCancelled,
            inputShadowText,

            processInputFill(e) {
                if (e === void 0) {
                    return;
                }

                if (e.keyCode === 27) {
                    if (inputFillCancelled.value !== true) {
                        inputFillCancelled.value = true;
                    }
                } else if (e.keyCode === 9) {
                    if (inputFillCancelled.value !== true && this.inputShadowText.length > 0) {
                        stopAndPrevent(e);
                        inputModel.value = (typeof inputModel.value === "string" ? inputModel.value : "") + this.inputShadowText;
                    }
                } else if (inputFillCancelled.value === true) {
                    inputFillCancelled.value = false;
                }
            },

            textareaModel,
            textareaFillCancelled,
            textareaShadowText,

            processTextareaFill(e) {
                if (e === void 0) {
                    return;
                }

                if (e.keyCode === 27) {
                    if (textareaFillCancelled.value !== true) {
                        textareaFillCancelled.value = true;
                    }
                } else if (e.keyCode === 9) {
                    if (textareaFillCancelled.value !== true && this.textareaShadowText.length > 0) {
                        stopAndPrevent(e);
                        textareaModel.value = (typeof textareaModel.value === "string" ? textareaModel.value : "") + this.textareaShadowText;
                    }
                } else if (textareaFillCancelled.value === true) {
                    textareaFillCancelled.value = false;
                }
            },
        };
    },
};
</script>
