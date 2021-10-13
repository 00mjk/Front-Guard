<template>
    <div class="sector-route q-px-md">
        <div v-if="Walk">
            <div class="row">
                <div class="sector-time">
                    <p class="legend">{{ Hour }}</p>
                </div>

                <div class="sector-line center">
                    <span class="iconify" data-icon="mdi:walk" style="color: #486a89" data-width="30" data-height="30"></span>
                </div>

                <div class="sector-text q-pl-sm">
                    <label> {{ BusStop }}</label>
                </div>
            </div>

            <div class="row">
                <div class="sector-time"></div>

                <div class="sector-line center q-mt-sm">
                    <img src="../assets/Line215.svg" class="moneco" />
                </div>

                <div class="sector-text q-pl-sm">
                    <legend>{{ Distance }} m</legend>
                    <legend>about {{ Time }} minutes</legend>
                </div>
            </div>
        </div>
        <div v-else>
            <div v-if="!Walk && !Final">
                <div class="row">
                    <div class="sector-time">
                        <p class="legend">{{ Hour }}</p>
                    </div>

                    <div class="sector-line center">
                        <line-number :Color="Color" :Line="Line" />
                    </div>

                    <div class="sector-text q-pl-sm">
                        <label>{{ BusStop }}</label>
                    </div>
                </div>

                <div class="row">
                    <div class="sector-time"></div>

                    <div class="sector-line center q-mt-sm" style="margin-top: -2px"><span :style="styles" class="col-line"> </span></div>

                    <div class="sector-text q-pl-sm">
                        <legend>{{ BusStops }} bus stops</legend><br>
                        <legend>{{ Time }} minutes</legend>
                    </div>
                </div>
            </div>
        </div>

        <div v-if="Final">
            <div class="row">
                <div class="sector-time">
                    <p class="legend">{{ Hour }}</p>
                </div>

                <div class="sector-line center">
                    <img style="height: 25px" src="../assets/end_journey.svg" class="moneco" />
                </div>

                <div class="sector-text q-pl-sm">
                    <label>{{ BusStop }}</label>
                </div>
            </div>

            <div class="row">
                <div class="col-md-2 col-sm-2"></div>

                <div class="col-md-2 col-sm-2 center"></div>

                <div class="col-md-8 col-sm-2"></div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.sector-time,
.sector-line,
.sector-text {
    display: flex;
    align-items: center;
}

.sector-time {
    width: 40px;

    p {
        color: #686868;
    }
}

.sector-line {
    width: 40px;
}

.sector-text {
    width: calc(100% - 80px);
}

.col-line::before {
    content: "";
    display: inline-block;
    height: 55px;
}
</style>

<script>
import { defineComponent } from "@vue/composition-api";
import LineNumber from "./LineNumber.vue";

export default defineComponent({
    components: { LineNumber },
    props: {
        Type: String,
        Distance: String,
        Time: String,
        Line: String,
        Color: String,
        BusStop: String,
        BusStops: String,
        Walk: String,
        Number: String,
        Hour: String,
        Final: String,
    },
    computed: {
        style() {
            return "background: " + this.Color + ";";
        },
        styles() {
            return "border: 2px solid " + this.Color + ";";
        },
    },

    setup() {
        return {};
    },
});
</script>
