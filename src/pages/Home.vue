<template>
    <q-page class="doc-page" style="max-width: 1440px; margin: 0 auto; min-height: 0px; padding: 0 16px">
        <div class="row row-breadcrumb">
            <div class="col q-py-md">
                <q-breadcrumbs gutter="none" style="">
                    <a href="./"> <q-breadcrumbs-el label="HOME" /></a>
                </q-breadcrumbs>
            </div>
        </div>

        <div class="row row-banner-home">
            <div class="col-md-12 col-sm-12 banner-home">
                <h4>Welcome Fahrgast!</h4>
                <h1 class="saludo">Where are you <span>going?</span></h1>
            </div>

            <!-- <div class="col-md-6 col-sm-12">
                <img src="../assets/wolfsburg-hero.png" class="max-width100" />
            </div> -->
        </div>

        <div class="row row-alerts-home">
            <div class="col-md-4 col-sm-8 col-xs-12">
                <div class="cardalert">
                    <div class="q-pa-md">
                        <div class="contenedorSlider">
                            <h4 class="">Alerts<span>.</span></h4>

                            <q-carousel v-model="slide" swipeable animated :control-type="controlType" control-color="dark" navigation padding arrows height="150px" class="text-purple rounded-borders">
                                <q-carousel-slide name="style" class="column">
                                    <div class="alert-title q-mt-md text-black text-weight-bold">
                                        <span class="icon-title"><q-icon name="warning" class="text-orange" /></span>
                                        <span>Failure of the passenger information display 1</span>
                                    </div>

                                    <div class="alert-text q-mt-sm text-black">Due to technical problems, the passenger information display may fail in the entire city area. We apologize for the inconvenience and ask for your understanding.</div>
                                </q-carousel-slide>
                                <q-carousel-slide name="tv" class="column">
                                    <div class="alert-title q-mt-md text-black text-weight-bold">
                                        <span class="icon-title"><q-icon name="warning" class="text-orange" /></span>
                                        <span>Failure of the passenger information display 2</span>
                                    </div>

                                    <div class="alert-text q-mt-sm text-black">Due to technical problems, the passenger information display may fail in the entire city area. We apologize for the inconvenience and ask for your understanding.</div>
                                </q-carousel-slide>
                                <q-carousel-slide name="layers" class="column">
                                    <div class="alert-title q-mt-md text-black text-weight-bold">
                                        <span class="icon-title"><q-icon name="warning" class="text-orange" /></span>
                                        <span>Failure of the passenger information display 3</span>
                                    </div>

                                    <div class="alert-text q-mt-sm text-black">Due to technical problems, the passenger information display may fail in the entire city area. We apologize for the inconvenience and ask for your understanding.</div>
                                </q-carousel-slide>
                            </q-carousel>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <form class="q-mt-xl trip-planner">
            <div class="row q-mb-lg">
                <div class="col-md-12 col-sm-12">
                    <h4>Trip planner<span class="color-point">.</span></h4>
                    <p class="p-body2">Routes from Monday to Saturday</p>
                </div>
            </div>

            <div class="row q-col-gutter-lg q-mb-xl">
                <div class="col-md-6 col-sm-12 col-xs-12">
                    <q-card class="my-card">
                        <input-generico-home class="label-title" Header="From" Hint="Write the name of the street, bus stop or activate your location" Label="Street/Line" />
                    </q-card>
                </div>
                <div class="col-md-6 col-sm-12 col-xs-12">
                    <q-card class="my-card">
                        <input-generico-home class="label-title" Header="To" Hint="Write the name of the street, bus stop or activate your location" Label="Street/Line" />
                    </q-card>
                </div>
            </div>

            <div class="row q-col-gutter-md">
                <div class="col-md-12 col-sm-12">
                    <p>I´D LIKE TO</p>
                </div>
            </div>

            <div class="row q-col-gutter-lg q-mb-xl">
                <div class="col-md-6 col-sm-12 col-xs-12 block-like-to">
                    <div class="radio-toolbar">
                        <input type="radio" id="radioApple" name="radioFruit" value="DEPART" checked />
                        <label class="q-mr-lg" for="radioApple">DEPART</label>

                        <input type="radio" id="radioBanana" name="radioFruit" value="ARRIVE" />
                        <label class="q-mr-lg" for="radioBanana">ARRIVE</label>

                        <input type="radio" id="radioOrange" name="radioFruit" value="REGULAR JORNEY" />
                        <label class="q-mr-lg" for="radioOrange">REGULAR JORNEY</label>
                    </div>
                </div>

                <div class="col-md-3 col-sm-6 col-xs-12">
                    <time-input class="label-title" Header="At"> </time-input>
                </div>

                <div class="col-md-3 col-sm-6 col-xs-12">
                    <date-input class="label-title" Header="On" />
                </div>
            </div>

            <div class="row">
                <div class="col-md-12">
                    <input style="float: right" type="button" class="btnsubmit" onclick="location.href='../#/TripPlanner'" value="Plan My trip" />
                </div>
            </div>
        </form>

        <form>
            <div class="row row-bus-lines-info q-col-gutter-md">
                <div class="col-md-12 col-sm-12 q-mb-lg">
                    <h4>Bus lines info<span class="color-point">.</span></h4>
                    <p class="p-body2">Routes from Monday to Saturday</p>
                </div>
            </div>

            <div class="row q-col-gutter-lg">
                <div class="col-md-8 col-sm-12">
                    <search-input Header="Label" />

                    <div class="busCards q-mt-lg">
                        <bus-card class="line-201" Color="var(--c201)" Numero="201" Label1="Velstove" Label2="Mörser Winkel" />
                        <bus-card class="line-202" Color="var(--c202)" Numero="202" Label1="Velstove" Label2="Mörser Winkel" />
                        <bus-card class="line-203" Color="var(--c203)" Numero="203" Label1="Velstove" Label2="Mörser Winkel" />
                        <bus-card class="line-204" Color="var(--c204)" Numero="204" Label1="Velstove" Label2="Mörser Winkel" />
                        <bus-card class="line-211" Color="var(--c211)" Numero="211" Label1="Velstove" Label2="Mörser Winkel" />
                        <bus-card class="line-212" Color="var(--c212)" Numero="212" Label1="Velstove" Label2="Mörser Winkel" />
                        <bus-card class="line-213" Color="var(--c213)" Numero="213" Label1="Velstove" Label2="Mörser Winkel" />
                        <bus-card class="line-215" Color="var(--c215)" Numero="215" Label1="Velstove" Label2="Mörser Winkel" />
                        <bus-card class="line-216" Color="var(--c216)" Numero="216" Label1="Velstove" Label2="Mörser Winkel" />
                        <bus-card class="line-218" Color="var(--c218)" Numero="218" Label1="Velstove" Label2="Mörser Winkel" />
                    </div>
                </div>

                <div class="col-md-4 col-xs-12">
                    <div class="q-card my-card">
                        <google-maps />
                    </div>
                </div>
            </div>
        </form>
    </q-page>
</template>

<script>
import { ref } from "vue";
import InputGenericoHome from "src/components/InputGenericoHome.vue";
import DateInput from "src/components/DateInputOn.vue";
import TimeInput from "src/components/TimeInput.vue";
import SearchInput from "src/components/SearchInput.vue";
import BusCard from "src/components/BusCard.vue";
import GoogleMaps from "src/components/GoogleMaps.vue";

export default {
    components: {
        InputGenericoHome,
        DateInput,
        TimeInput,
        SearchInput,
        BusCard,
        GoogleMaps,
    },
    setup() {
        return {
            search: ref(""),
            model: ref("one"),
            secondModel: ref("one"),
            controlType: ref("flat"),
            controlTypeOptions: [
                { value: "regular", label: "regular" },
                { value: "unelevated", label: "unelevated" },
                { value: "flat", label: "flat (default)" },
                { value: "outline", label: "outline" },
                { value: "push", label: "push" },
            ],

            slide: ref("style"),
            lorem: "Failure of the passenger information display ",
        };
    },
};
</script>

<style lang="scss" scoped>
.my-custom-toggle {
    border: 1px solid #027be3;
}

/* START form trip planner */
.trip-planner {
    border-bottom: 1px solid var(--neutral-40);
    padding-bottom: 80px;
}
/* END form trip planner */
</style>
