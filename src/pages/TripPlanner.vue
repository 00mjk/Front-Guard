<template>
    <q-page class="doc-page" style="max-width: 1440px; margin: 0 auto; min-height: 0px; padding: 16px">
        <div class="row row-breadcrumb">
            <div class="col q-py-md">
                <q-breadcrumbs gutter="none">
                    <a href="./">
                        <q-breadcrumbs-el label="HOME / TRIP PLANNER" />
                    </a>
                </q-breadcrumbs>
            </div>
        </div>

        <div class="row q-col-gutter-md q-mb-sm">
            <div class="col-md-12 col-sm-12 q-mb-lg">
                <h4>Trip planner<span class="color-point">.</span></h4>
                <p class="p-body2">Routes from Monday to Saturday</p>
            </div>
        </div>

        <div class="row q-col-gutter-lg">
            <div class="col-md-3 col-sm-12 col-xs-12 q-mb-lg">
                <input-generico-home Header="From" Hint="Write the name of the street, bus stop or your location " Label="Leonardo Hotel Wolfsburg City Center" />
                <input-generico-home class="q-mt-lg" Label="Volkswagen AutoMuseum" Hint="Write the name of the street or bus stop" Header="To" />

                <div class="more-options q-mt-md p-body2">
                    <a href="">MORE OPTIONS <span class="iconify" data-icon="mdi:plus-circle-outline"></span></a>
                </div>

                <card-results class="q-mt-md" Min="27" Depart="11:47" Arrive="12:14" Price="2,90" />
                <card-results class="q-mt-md" Min="28" Depart="12:16" Arrive="12:44" Price="2,90" />
                <card-results class="q-mt-md" Min="24" Depart="12:20" Arrive="12:44" Price="2,90" />
                <card-results class="q-mt-md" Min="28" Depart="12:46" Arrive="13:14" Price="2,90" />
                <card-results class="q-mt-md" Min="24" Depart="12:50" Arrive="13:14" Price="2,90" />
            </div>

            <div class="col-md-9 col-sm-12 col-xs-12 q-mb-lg">
                <div class="mapa">
                    <div class="q-pa-md">
                        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d11912.084941383731!2d10.801808852063795!3d52.426292973821795!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47af93c8d01e69e5%3A0xe2465df60ba210ae!2sVolkswagen-Arena!5e0!3m2!1ses!2ses!4v1632827773646!5m2!1ses!2ses" allowfullscreen="" loading="lazy" key="" style="min-height: 849px; border: 0; height: 100%; width: 100%"></iframe>
                    </div>
                </div>

                <div class="row">
                    <div class="col-md-4 col-sm-6 col-xs-12 q-mb-lg q-ma-xl">
                        <card-map Header="Imperial" />
                    </div>
                    <div class="col-md-1"></div>
                    <div class="col-md-4 col-sm-6 col-xs-12 q-mb-lg q-ma-xl">
                        <line-card Header="WVG-08821" />
                    </div>
                </div>
            </div>
        </div>
    </q-page>
</template>

<script>
import { defineComponent } from "@vue/composition-api";
import CardMap from "src/components/CardMap.vue";
import CardResults from "src/components/CardResults.vue";
import InputGenericoHome from "src/components/InputGenericoHome.vue";
import LineCard from "src/components/LineCard.vue";

export default defineComponent({
    components: { InputGenericoHome, CardMap, CardResults, LineCard },
    setup() {},
});
</script>

<style lang="scss" scoped>
.more-options {
    a {
        display: flex;
        align-items: center;
        color: var(--neutral-40);
        gap: 8px;
        font-size: 14px;
        max-width: 120px;

        .iconify {
            font-size: 15px;
            color: var(--neutral-40);
            transition: var(--transition);
            margin-top: 1px;
        }

        &:hover {
            color: var(--neutral-80);

            .iconify {
                color: var(--neutral-80);
                transform: rotate(270deg);
            }
        }
    }
}

.mapa {
    border-radius: 16px;
}
</style>
