<template>
  <a
    style="text-decoration: none; color: #686868"
    href="../#/TripPlanner/LineInfo"
  >
    <q-card class="my-card" style="height: 374px; width: 360px">
      <q-card-section class="headercardmap" style="display: flex">
        <div class="row">
          <div class="col-md-12" style="width: 100%">
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
              <div class="col" style="display: inherit">
                <legend class="q-mb-sm">LINE :</legend>
                <line-number
                  Line="201"
                  Color="#D41217"
                  class="q-mr-xs q-mb-sm"
                  style="margin-left: 10px"
                />
              </div>
              <div class="col">
                <legend class="q-mb-sm">
                  DESTINATION : <span class="destination"> WENDSCHOTT</span>
                </legend>
              </div>
            </div>
            <div style="width: 100%" class="col col-lineheader"></div>

            <div class="row">
              <div class="col-md-4">
                <legend class="q-mb-sm">NEXT STOP :</legend>
                <legend class="destination">Kaufhof</legend>
              </div>
              <div class="row" style="width: 100%">
                <div class="col">
                  <label> with correspondence </label>
                </div>
                <div class="col">
                  <img src="../assets/Circleslines.svg" />
                </div>
              </div>
            </div>

            <div style="width: 100%" class="col col-lineheader"></div>
            <div class="row">
              <div class="col-md-12" style="width: 100%">
                <legend class="q-mb-sm">OCCUPANCY :</legend>
                <div class="row" style="width: 100%">
                  <div class="col-md-6">
                    <img src="../assets/Seats.svg" />
                  </div>
                  <div class="col-md-6">
                    <p class="p-body2" style="text-align: right;color: #F8CA00;">75%</p>
                  </div>
                </div>
              </div>
            </div>

            <div style="width: 100%" class="col col-lineheader"></div>
            <div class="row">
              <div class="col-md-12">
                <legend class="q-mb-sm">BUS INFO :</legend>

                <div class="row">
                  <Icon color="#CDCDCD" class="q-mr-md" icon="mdi:wheelchair-accessibility" />
                  <Icon color="#CDCDCD"  class="q-mr-md" icon="mdi:baby-buggy" />
                  <Icon color="#CDCDCD" class="q-mr-md" icon="mdi:car-child-seat" />
                  <Icon color="#CDCDCD" class="q-mr-md" icon="mdi:air-conditioner" />
                  <Icon color="#CDCDCD" class="q-mr-md" icon="mdi:wifi-star" />
                  <Icon color="#CDCDCD" class="q-mr-md" icon="mdi:bicycle" />
                  <Icon color="#CDCDCD" class="q-mr-md" icon="mdi:heart-flash" />
                </div>
              </div>
            </div>
          </div>

          <div class="row">
            <div style="width: 100%" class="col col-lineheader"></div>
            <div class="col-md-12">
              <legend class="q-mb-sm q-mt-md">COVID PROTOCOL :</legend>
              <div class="row">
                <Icon  color="#CDCDCD" class="q-mr-md" icon="mdi:face-mask" />
                <Icon  color="#CDCDCD" class="q-mr-md" icon="mdi:social-distance-2-meters" />
                <Icon color="#CDCDCD" class="q-mr-md" icon="mdi:hand-wash" />
              </div>
            </div>
          </div>
        </div>
      </q-card-section> </q-card
  ></a>
</template>

<script>
import { defineComponent } from "@vue/composition-api";
import LineNumber from "./LineNumber.vue";
import { Icon } from "@iconify/vue";

export default defineComponent({
  components: { LineNumber, Icon },
  props: {
    Header: String,
  },
  setup() {},
});
</script>

<style scoped>
.destination {
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
legend{
  font-style: normal;
font-weight: normal;
line-height: 15px;
/* identical to box height */

letter-spacing: 0.05em;
color: #686868
}
</style>
