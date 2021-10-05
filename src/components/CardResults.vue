<template>
  <q-list bordered class="rounded-borders">
    <q-expansion-item>
      <template v-slot:header class="wrap">
        <q-item-section avatar style="display: inline; padding-top: 8px">
          <img class="moneco" src="../assets/Walk.svg" />
          <div class="box moneco">
            <p class="numero">212</p>
          </div>
          <img class="moneco" src="../assets/Walk.svg" />
        </q-item-section>

        <q-item-section style="align-items: end">
          <div class="row items-center" style="margin-top: -6px">
            <div style="display: block">
              <p class="headerNumber">27</p>
              <legend style="margin-top: -7px">MIN</legend>
            </div>
          </div>
        </q-item-section>

        <div class="row" style="width: 100%; margin-top: 20px">
          <div class="col-md-4" style="width: 33%">
            <legend>
              DEPART
              <span class="date">
                12:20 <img src="../assets/Group55.svg" style="margin-left: 8px"
              /></span>
            </legend>
          </div>

          <div class="col-md-4" style="width: 33%">
            <legend>
              ARRIVE
              <span class="date"> 13:14 </span>
            </legend>
          </div>

          <div class="col-md-4" style="width: 33%">
            <legend style="width: 100%; display: flex; justify-content: right;">
              <span style="display: flex" class="date">
                2,90 € <img src="../assets/Info.svg" style="margin-left: 4px" />
              </span>
            </legend>
          </div>
        </div>
      </template>

      <q-card>
        <q-card-section>
          <div class="logos">
            <img src="../assets/Download.svg" style="margin-right: 10px" />
            <img src="../assets/Link.svg" style="margin-right: 10px" />
            <img src="../assets/Print.svg" />
          </div>
        </q-card-section>
               <card-results-line Time="9" Distance="520" BusStop="Leonardo Hotel Wolfsburg City Center" Type="Walk" Color="Blue"/>
               <card-results-line BusStop="Kuntsmuseum" BusStops="7" Time="7" />
               <card-results-line />
               <card-results-line />

        <q-card-section> 
        
        </q-card-section>
      </q-card>
    </q-expansion-item>
  </q-list>
</template>

<script>
import { defineComponent } from "@vue/composition-api";
import CardResultsLine from "./CardResultsLine.vue";

export default defineComponent({
  components: {CardResultsLine},
  setup() {},
});
</script>

<style>
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

.numero {
  font-family: Source Sans Pro;
  font-style: normal;
  font-weight: 600;
  font-size: 16px;
  line-height: 20px;
  justify-content: center;
  text-align: center;

  /* Neutral (Dark)/00 */

  color: #ffffff;
}
</style>
