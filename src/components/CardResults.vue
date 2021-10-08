<template>
  <q-list class="rounded-borders">
    <q-expansion-item>
      <template v-slot:header class="wrap">
        <q-item-section avatar style="display: inline; padding-top: 8px">
          <img class="moneco" src="../assets/Walk.svg" />
          <line-number Color="#F07E12" Line="201" class="moneco" />
          <img class="moneco" src="../assets/Walk.svg" />
        </q-item-section>

        <q-item-section style="align-items: end">
          <div class="row items-center" style="margin-top: -6px">
            <div style="display: block">
              <p class="headerNumber">{{ Min }}</p>
              <legend style="margin-top: -7px">MIN</legend>
            </div>
          </div>
        </q-item-section>

        <div class="row" style="width: 100%">
          <div style="width: 100%" class="col col-lineheader"></div>
        </div>

        <div class="row" style="width: 100%; margin-top: 10px">
          <div class="col-md-4" style="width: 33%">
            <legend>
              DEPART
              <span class="date">
                {{ Depart }}
                <img src="../assets/Group55.svg" style="margin-left: 8px"
              /></span>
            </legend>
          </div>

          <div class="col-md-4" style="width: 33%">
            <legend>
              ARRIVE
              <span class="date"> {{ Arrive }} </span>
            </legend>
          </div>

          <div class="col-md-4" style="width: 33%">
            <legend style="width: 100%; display: flex; justify-content: right">
              <span style="display: flex" class="date">
                {{ Price }} €
                <img src="../assets/Info.svg" style="margin-left: 4px" />
              </span>
            </legend>
          </div>
        </div>
      </template>

      <q-card>
        <q-card-section>
          <div class="logos">
            <div class="row" style="width: 100%">
              <div
                style="width: 100%; margin-top: -16px"
                class="col col-lineheader"
              ></div>
            </div>
            <img src="../assets/Download.svg" style="margin-right: 10px" />
            <img src="../assets/Link.svg" style="margin-right: 10px" />
            <img src="../assets/Print.svg" />
          </div>
        </q-card-section>

        <card-results-line
          Hour="12:20"
          Time="9"
          Distance="520"
          BusStop="Leonardo Hotel Wolfsburg City Center"
          Walk="true"
        />
        <card-results-line
          Hour="12:29"
          Line="201"
          Color="#D41217"
          Number="201"
          BusStop="Kuntsmuseum"
          BusStops="7"
          Time="7"
        />
        <card-results-line
          Hour="12:36"
          Line="212"
          BusStop="ZOB Bay 8"
          BusStops="1"
          Number="212"
          Time="2"
          Color="#F07E12"
        />
        <card-results-line
          Hour="12:38"
          Walk="true"
          BusStop="Feuerwehr"
          Distance="300"
          Time="6"
        />
        <card-results-line
          Hour="12:38"
          Final="true"
          BusStop="Volkswagen AutoMuseum"
        />

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

<style>
body.desktop .q-focus-helper {
  background: none;
  opacity: 1;
  border: 1px solid rgba(235, 46, 45, 0.6);
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
  border-bottom-left-radius: 0;
  border-bottom-right-radius: 0;
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
}

body.desktop .q-focusable:focus > .q-focus-helper::before,
body.desktop .q-manual-focusable--focused > .q-focus-helper::before,
body.desktop .q-hoverable:hover > .q-focus-helper::before {
  opacity: 1;
  width: 100%;
  margin: 0;
}

body.desktop .q-focusable:focus > .q-focus-helper::after,
body.desktop .q-manual-focusable--focused > .q-focus-helper::after,
body.desktop .q-hoverable:hover > .q-focus-helper::after {
  opacity: 0;
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

legend {
  font-family: Source Sans Pro;
  font-style: normal;
  font-weight: normal;
  font-size: 12px;
  line-height: 15px;
  /* identical to box height */

  /* Neutral (Dark)/40 */

  color: #9a9a9a;
}
.date {
  color: #282828;
  font-size: 14px;
}

.no-wrap {
  flex-wrap: wrap !important;
}
.moneco {
  float: left;
}
.rounded-borders {
  background: #ffffff;
  /* Shadow/Shadow Card Form */

  box-shadow: 0px 8px 16px rgba(17, 17, 17, 0.06);
  border-radius: 16px;
}

.q-expansion-item__toggle-icon {
  display: none;
}

.headerNumber {
  font-family: Source Sans Pro;
  font-style: normal;
  font-weight: bold;
  font-size: 21px;
  line-height: 140%;
  /* or 29px */

  text-align: center;

  /* Neutral (Dark)/80 */

  color: #282828;
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
