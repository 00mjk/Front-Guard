<template>
  <q-page
    class="doc-page"
    style="max-width: 1440px; margin: 0 auto; min-height: 0px; padding: 16px"
  >
    <div class="row q-col-gutter-md">
      <div class="col">
        <q-breadcrumbs
          gutter="none"
          style="
            font-family: Source Sans Pro;
            font-style: normal;
            font-weight: normal;
            font-size: 12px;
            line-height: 15px;
            color: #282828;
          "
        >
          <q-breadcrumbs-el label="HOME / TRIP PLANNER" />
        </q-breadcrumbs>
      </div>
    </div>

    <div class="row q-col-gutter-md" style="margin-top: 61px">
      <div class="col-md-2 col-sm-6 q-mb-lg">
        <h4>Trip planner<span style="color: #d92127">.</span></h4>
        <p class="p-body2">Routes from Monday to Saturday</p>
      </div>
    </div>

    <div class="row q-col-gutter-md" style="margin-top: 8px">
      <div class="col-md-3 col-sm-12 col-xs-12 q-mb-lg">
        <input-generico-home
          Header="From"
          Hint="Write the name of the street, bus stop or your location "
          Label="Leonardo Hotel Wolfsburg City Center"
        />
        <input-generico-home
          Label="Volkswagen AutoMuseum"
          Hint="Write the name of the street or bus stop"
          Header="To"
          style="margin-top: 16px"
        />

        <p class="p-body2" style="color: #9a9a9a; margin-top: 16px">
          MORE OPTIONS <img src="../assets/Pluscircle.svg" />
        </p>

        <card-results
          class="q-mt-md"
          Min="27"
          Depart="11:47"
          Arrive="12:14"
          Price="2,90"
        />
        <card-results
          class="q-mt-md"
          Min="28"
          Depart="12:16"
          Arrive="12:44"
          Price="2,90"
        />
        <card-results
          class="q-mt-md"
          Min="24"
          Depart="12:20"
          Arrive="12:44"
          Price="2,90"
        />
        <card-results
          class="q-mt-md"
          Min="28"
          Depart="12:46"
          Arrive="13:14"
          Price="2,90"
        />
        <card-results
          class="q-mt-md"
          Min="24"
          Depart="12:50"
          Arrive="13:14"
          Price="2,90"
        />
      </div>

      <div class="col-md-9 col-sm-12 col-xs-12 q-mb-lg">
        <div class="mapa">
          <div class="q-pa-md">
            <iframe
              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d11912.084941383731!2d10.801808852063795!3d52.426292973821795!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47af93c8d01e69e5%3A0xe2465df60ba210ae!2sVolkswagen-Arena!5e0!3m2!1ses!2ses!4v1632827773646!5m2!1ses!2ses"
              allowfullscreen=""
              loading="lazy"
              key=""
              style="min-height: 849px; border: 0; height: 100%; width: 100%"
            ></iframe>
          </div>
        </div>

        <div class="row">
          <div class="col-md-4 col-sm-12 col-xs-12 q-mb-lg q-ma-xl">
            <card-map Header="Rathaus" />
          </div>

          <div class="col-md-4 col-sm-12 col-xs-12 q-mb-lg q-ma-xl">
            <card-map />
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

export default defineComponent({
  components: { InputGenericoHome, CardMap, CardResults },
  setup() {},
});
</script>
