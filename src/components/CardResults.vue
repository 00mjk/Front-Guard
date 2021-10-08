<template>
    <q-list class="rounded-borders">
        <q-expansion-item>
            <template v-slot:header class="wrap">
                <div class="row bus-route">
                    <q-item-section avatar class="q-pr-none">
                        <img class="moneco" src="../assets/Walk.svg" />
                        <line-number Line="212" Color="#F07E12" >
                        <img class="moneco" src="../assets/Walk.svg" />
                    </q-item-section>

                    <q-item-section class="time-route">
                        <!-- <p class="headerNumber">{{ Min }}</p> -->
                        <p class="headerNumber"></p>
                        <span class="legend" style="">MIN</span>
                    </q-item-section>
                </div>

                <div class="row q-mt-sm info-route">
                    <div class="depart-arrive-route">
                        <div class="depart-route">
                            <p class="legend">
                                DEPART:
                                <span class="date">
                                    {{ Depart }}
                                </span>
                            </p>
                        </div>

                        <div class="arrow">
                            <img src="../assets/Group55.svg" />
                        </div>

                        <div class="arrive-route">
                            <p class="legend">
                                ARRIVE:
                                <span class="date"> {{ Arrive }} </span>
                            </p>
                        </div>
                    </div>

                    <div class="price-route">
                        <p class="legend">
                            <span class="date">{{ Price }} €</span>
                        </p>
                        <p class="info-tarif">
                            <a href="#"><img src="../assets/Info.svg" /></a>
                        </p>
                    </div>
                </div>
            </template>

            <q-card>
                <q-card-section>
                    <div class="actions">
                        <a href="#"><img src="../assets/Download.svg" /></a>
                        <a href="#"><img src="../assets/Link.svg" /></a>
                        <a href="#"><img src="../assets/Print.svg" /></a>
                    </div>
                </q-card-section>

                <card-results-line Hour="12:20" Time="9" Distance="520" BusStop="Leonardo Hotel Wolfsburg City Center" Walk="true" />
                <card-results-line Hour="12:29" Line="201" Color="#D41217" Number="201" BusStop="Kuntsmuseum" BusStops="7" Time="7" />
                <card-results-line Hour="12:36" Line="212" BusStop="ZOB Bay 8" BusStops="1" Number="212" Time="2" Color="#F07E12" />
                <card-results-line Hour="12:38" Walk="true" BusStop="Feuerwehr" Distance="300" Time="6" />
                <card-results-line Hour="12:38" Final="true" BusStop="Volkswagen AutoMuseum" />

                <q-card-section> </q-card-section>
            </q-card>
        </q-expansion-item>
    </q-list>
</template>

<script>
import { defineComponent } from "@vue/composition-api";
import CardResultsLine from "./CardResultsLine.vue";
import LineNumber from "./LineNumber.vue";

export default defineComponent({
    components: { CardResultsLine, LineNumber },
    props: {
        Min: String,
        Depart: String,
        Arrive: String,
        Price: String,
    },
    setup() {},
});
</script>

<style lang="scss">
.q-list {
    transition: all ease-in-out 0.2s;

    &:hover {
        background: #fff;
        opacity: 1;
        margin-top: 18px;
        margin-bottom: -2px;
        box-shadow: 0px 3px 6px rgba(17, 17, 17, 0.1);
    }

    .q-item {
        border: 5px solid #fff;
        border-radius: 16px;

        .bus-route {
            display: flex;
            align-items: center;
            justify-content: space-between;
            width: 100%;
            border-bottom: 1px dashed #eee;
            padding-bottom: 10px;

            .q-item__section {
                display: flex;
                align-items: center;
                flex-direction: inherit;
                height: 40px;
                gap: 5px;
            }

            .time-route {
                flex: none;
                justify-content: center;
                height: 40px;

                .headerNumber {
                    font-family: Source Sans Pro;
                    font-style: normal;
                    font-weight: bold;
                    font-size: 21px;
                    line-height: 40px;
                    text-align: right;
                    color: #999;
                    height: 40px;
                    width: 40px;
                    position: relative;
                    transition: all ease-in-out 0.3s;

                    &::before {
                        content: "28";
                        position: absolute;
                        width: 40px;
                        top: 0;
                        left: 0;
                        height: 40px;
                        line-height: 38px;
                        transition: all ease-in-out 0.3s;
                    }

                    &::after {
                        content: "28";
                        position: absolute;
                        width: 40px;
                        top: 20px;
                        left: 0;
                        height: 40px;
                        line-height: 38px;
                        opacity: 0;
                        transition: all ease-in-out 0.3s;
                    }
                }
            }
        }

        .info-route {
            width: 100%;
            justify-content: space-between;
            align-items: center;

            .depart-arrive-route,
            .price-route {
                display: flex;
                align-items: center;
                gap: 10px;
                transition: all ease-in-out 0.3s;

                a {
                    display: flex;
                    align-items: center;
                }
            }
        }

        &:hover {
            border: 5px solid #fff;
            background-color: #f6f6f6;

            .bus-route {
                border-bottom: 1px dashed #ddd;

                .time-route .headerNumber {
                    color: #282828;

                    &::before {
                        top: -20px;
                        opacity: 0;
                    }

                    &::after {
                        top: 0;
                        opacity: 1 !important;
                    }
                }
            }

            .info-route {
                .legend {
                    color: #666;
                }

                .date {
                    color: #282828;
                }
            }
        }
    }

    .q-expansion-item--expanded {
        .q-item {
            border: 5px solid #fff;
            background-color: #f6f6f6;

            .time-route .headerNumber {
                color: #282828;
            }

            .info-route {
                .legend {
                    color: #666;
                }

                .date {
                    color: #282828;
                }
            }
        }

        .q-expansion-item__content {
            .q-card {
                background: none;

                .q-card__section {
                    padding: 8px 16px 12px;
                }

                .actions {
                    display: flex;
                    align-items: center;
                    gap: 16px;

                    a {
                        display: flex;
                        align-items: center;
                    }
                }
            }
        }
    }

    .legend {
        font-family: Source Sans Pro;
        font-style: normal;
        font-weight: normal;
        font-size: 12px;
        line-height: 15px;
        color: #aaa;
        transition: all ease-in-out 0.3s;

        .date {
            color: #999;
            font-size: 14px;
            padding-left: 5px;
            font-weight: 600;
            transition: all ease-in-out 0.3s;
        }
    }
}

body.desktop .q-focus-helper {
    background: none;
    opacity: 1;
    top: 0;
    left: 0;
    border-radius: 16px;
    transition: all ease-in-out 0.3s;
    pointer-events: none;
}

body.desktop .q-focus-helper {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    pointer-events: none;
    border-radius: inherit;
    opacity: 0;
    transition: all ease-in-out 0.3s;
    border-radius: 16px;
    overflow: hidden;
}

body.desktop .q-focusable:focus > .q-focus-helper,
body.desktop .q-manual-focusable--focused > .q-focus-helper,
body.desktop .q-hoverable:hover > .q-focus-helper {
    background: none;
    opacity: 1;
}

body.desktop .q-focus-helper::before {
    background: none;
    width: 1px;
    background: #d92127;
    height: 3px;
    margin: 0 50%;
    transition: all ease-in-out 0.3s;
    top: initial;
    bottom: 0;
    display: none;
}

body.desktop .q-focusable:focus > .q-focus-helper::before,
body.desktop .q-manual-focusable--focused > .q-focus-helper::before,
body.desktop .q-hoverable:hover > .q-focus-helper::before {
    opacity: 1;
    width: 100%;
    margin: 0;
    display: none;
}

body.desktop .q-focusable:focus > .q-focus-helper::after,
body.desktop .q-manual-focusable--focused > .q-focus-helper::after,
body.desktop .q-hoverable:hover > .q-focus-helper::after {
    opacity: 0;
    display: none;
}

.col-lineheader::before {
    content: "";
    display: inline-block;

    width: 100%;

    border: 1px dashed #f2f2f2;
}

.mxrig {
    width: 100%;
    float: right;
}

.center {
    justify-content: center;
    align-items: center;
    display: flex;
}

.no-wrap {
    flex-wrap: wrap !important;
}
.moneco {
    float: left;
}
.rounded-borders {
    background: #ffffff;

    box-shadow: 0px 8px 16px rgba(17, 17, 17, 0.06);
    border-radius: 16px;
}

.q-expansion-item__toggle-icon {
    display: none;
}

.box {
    background: #f07e12;
    border-radius: 8px;
    width: 40px;
    height: 26px;
    text-align: center;
    justify-content: center;
}
</style>
