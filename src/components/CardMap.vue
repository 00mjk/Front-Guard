<template>
  <q-card class="my-card" style="height: 374px; width: 360px; ">
    <q-card-section class="headercardmap">
      <div class="row">
        <div class="col-md-12">
          <img src="../assets/BusStop.svg" />

          <p style="color: #ffffff; display: inline" class="p-body1">
            {{ Header }}
          </p>
        </div>
      </div>
    </q-card-section>
    <q-card-section>
      <div class="row">
        <div class="col-md-12">
          <div class="row">
            <line-number Line="201" Color="#D41217" class="q-mr-xs q-mb-sm" />
            <line-number Line="202" Color="#31B5A4" class="q-mr-xs q-mb-sm" />
            <line-number Line="203" Color="#6A509D" class="q-mr-xs q-mb-sm" />
            <line-number Line="204" Color="#EBB500" class="q-mr-xs q-mb-sm" />
            <line-number Line="211" Color="#21B9E6" class="q-mr-xs q-mb-sm" />
            <line-number Line="212" Color="#F07E12" class="q-mr-xs q-mb-sm" />
            <line-number Line="212" Color="#D41217" class="q-mr-xs q-mb-sm" />
            <line-number Line="212" Color="#D41217" class="q-mr-xs q-mb-sm" />
          </div>
          <div style="width: 100%" class="col col-lineheader"></div>
          <legend class="q-mb-sm">
            DESTINATION : <span class="destination"> WENDSCHOTT</span>
          </legend>
          <div class="row">
            <div class="col-md-4  col-sm-4 col-xs-4">
              <line-number Line="201" Color="#D41217" class="q-mr-xs q-mb-sm" />
              <line-number Line="204" Color="#EBB500" class="q-mr-xs q-mb-sm" />
              <line-number Line="212" Color="#097EC1" class="q-mr-xs q-mb-sm" />
            </div>
            <div class="col-md-4  col-sm-4 col-xs-4">
              <img src="../assets/Seats.svg" class="q-mb-sm q-mt-xs" />
              <img src="../assets/Seats.svg" class="q-mb-sm" />
              <img src="../assets/Seats.svg" />
            </div>
            <div class="col-md-4  col-sm-4 col-xs-4" style="text-align: end">
              <p class="p-body2 q-mb-xs">Inminent Arrival</p>
              <p class="p-body2 q-mb-xs">2 m</p>
              <p class="p-body2">5 m</p>
            </div>
          </div>
           <div style="width: 100%" class="col col-lineheader"></div>
          <legend class="q-mb-sm">
            DESTINATION : <span class="destination"> DETMERODE</span>
          </legend>
          <div class="row">
            <div class="col-md-4  col-sm-4 col-xs-4">
              <line-number Line="201" Color="#D41217" class="q-mr-xs q-mb-sm" />
              <line-number Line="204" Color="#EBB500" class="q-mr-xs q-mb-sm" />
              <line-number Line="212" Color="#097EC1" class="q-mr-xs q-mb-sm" />
            </div>
            <div class="col-md-4  col-sm-4 col-xs-4" >
              <img src="../assets/Seats.svg" class="q-mb-sm q-mt-xs" />
              <img src="../assets/Seats.svg" class="q-mb-sm" />
              <img src="../assets/Seats.svg" />
            </div>
            <div class="col-md-4  col-sm-4 col-xs-4 " style="text-align: end">
              <p class="p-body2 q-mb-xs">Inminent Arrival</p>
              <p class="p-body2 q-mb-xs">2 m</p>
              <p class="p-body2">5 m</p>
            </div>
          </div>
        </div>
      </div>
    </q-card-section>
  </q-card>
</template>

<script>
import { defineComponent } from "@vue/composition-api";
import LineNumber from "./LineNumber.vue";

export default defineComponent({
  components: { LineNumber },
  props: {
    Header: String,
    Line: String,

    Occupancy: String,
    Transfer: String,
  },
  setup() {},
});
</script>

<style scoped>
.destination{
  font-family: Source Sans Pro;
font-style: normal;
font-weight: normal;
font-size: 12px;
line-height: 15px;
/* identical to box height */

letter-spacing: 0.05em;

/* Neutral (Dark)/60 */

color: #282828;
font-weight: bold;
}



.headercardmap {
  height: 48px;

  /* Bus Lines/201 */

  background: #d41217;
  /* Shadow/Soft */

  box-shadow: 0px 8px 16px rgba(17, 17, 17, 0.04);
  border-radius: 12px 12px 0px 0px;

  /* Bus Lines/201 */

  background: #d41217;
  /* Shadow/Soft */

  box-shadow: 0px 8px 16px rgba(17, 17, 17, 0.04);
  border-radius: 12px 12px 0px 0px;
}

label {
  color: #9a9a9a;
}
</style>
