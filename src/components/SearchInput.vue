<template>
    <q-card class="my-card card-search">
        <div class="q-pa-md card-search-cont">
            <div class="form-card-search">
                <q-card-section>
                    <div class="label-title">{{ Header }}</div>
                </q-card-section>
                <div class="q-gutter-y-md column">
                    <q-input filled clearable color="dark" label="Label2"></q-input>
                </div>
            </div>

            <div class="btn-card-search">
                <input type="button" class="btnsubmit" value="Search" />
            </div>
        </div>
        <div class="q-pb-md q-px-md">
            <div class="container">
                <q-card-section class="q-pa-none">
                    <q-toggle class="p-body2 q-mr-xl" v-model="value" color="red" label="DayTime bus lines" left-label size="xs" />
                    <q-toggle class="p-body2 q-mr-xl" v-model="value1" color="red" label="Evening bus lines" left-label size="xs" />
                    <q-toggle class="p-body2 q-mr-xl" v-model="value2" color="red" label="Special lines" left-label size="xs" />
                </q-card-section>
            </div>
        </div>
    </q-card>
</template>

<script>
import { event } from "quasar";
import { ref } from "vue";

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
        return {
            value: ref(false),
            value1: ref(false),
            value2: ref(false),
        };
    },
};
</script>
