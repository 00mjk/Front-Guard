<template>
  <q-card class="my-card" style="height: 821px; max-width: 464px">
    <q-card-section>
      <div class="row">
        <div class="col-md-3">
          <line-number
            :Color="Color"
            Line="215"
            style="height: 109px; width: 81px"
          />
        </div>
        <div class="col-md-8">
          <p :style="style" class="p-body1">LINE {{ Line }}</p>
          <h4 style="size: 21px; margin-top: -5px">{{ FirstStop }}</h4>
          <h4 style="size: 21px; margin-top: -15px">{{ LastStop }}</h4>
           
           <div class="row">
             <Icon icon="ci:circle-check" color="#459a33" height="16" />
          <label style="color: #31a836; " class="q-ml-xs">
            Good service
          </label>
          </div>
        </div>
        <div class="col-md-1">

          <Icon   icon="mdi:download-box-outline" color="#9a9a9a" />
        </div>
      </div>
    </q-card-section>

    <q-card-section>
      <div class="row">
        <div class="col-md-7 col-sm-7 col-xs-7 ">
          <p class="p-body1">NEXT ARRIVALS</p>
          <p style="margin-top: 10px" class="p-body2">Kuntmuseum</p>
          <p style="margin-top: 10px" class="p-body2">
            Heiligendorf, Barnstorfer Straße
          </p>
          <p style="margin-top: 10px; margin-bottom: 20px" class="p-body2">
            Heiligendorf, Hasenmorgen
          </p>
        </div>

        <div class="col-md-5 col-sm-5 col-xs-5">
          <p class="p-body2" style="margin-top: 35px">3 min</p>
          <p style="margin-top: 8px" class="p-body2">7 min</p>
          <p style="margin-top: 10px" class="p-body2">12 min</p>
        </div>
      </div>

      <div class="row">
        <div class="col-md-12">
          <hr class="provisional" />
        </div>
      </div>

      <div class="row" style="margin-top: 20px">
        <div class="col-md-6 col-sm-6 col-xs-6">
          <p class="p-body1">BUS RATES</p>
          <p
            class="p-body2"
            style="font-weight: bold; color: #282828; margin-top: 10px"
          >
            Short-haul ticket
          </p>
          <p class="p-body2 q-mt-sm">3 stops after boarding</p>
        </div>
        <div class="col-md-6 col-sm-6 col-xs-6" style="text-align: right">
          <p class="p-body2"></p>
          <p style="margin-top: 35px; font-weight: bold" class="p-body2">
            Rate zone 20
          </p>
          <p class="p-body2 q-mt-sm">1,60 €</p>
        </div>
      </div>
      <div class="row">
        <div class="col-md-12 col-sm-12 col-xs-12">
          <hr class="provisional" />
        </div>
      </div>

      <div class="row" style="margin-top: 20px">
        <div class="col-md-6">
          <p
            class="p-body2"
            style="font-weight: bold; color: #282828; margin-top: 10px"
          >
            Individual tickets
          </p>
          <p class="p-body2 q-mt-sm">Adult</p>
          <div class="row">
            <div class="col-md-12 col-sm-12 col-xs-12">
              <hr class="provisional" />
            </div>
          </div>
          <p class="p-body2 q-mt-sm">Children (6-14 years)</p>
        </div>
        <div class="col-md-6 col-sm-6 col-xs-6" style="text-align: right">
          <p class="p-body2"></p>

          <p style="margin-top: 40px" class="p-body2 q-mt-sm">2,90 €</p>
          <div class="row">
            <div class="col-md-12 col-sm-12 col-xs-12">
              <hr class="provisional" />
            </div>
          </div>
          <p class="p-body2 q-mt-sm">1,70 €</p>
          <a href="./"
            ><p style="margin-top: 10px; color: #eb2e2d" class="p-body2">
              Table of all bus fares
            </p>
          </a>
        </div>
      </div>
      <div class="row">
        <div class="col-md-12 col-sm-12 col-xs-12">
          <hr class="provisional" />
        </div>
      </div>

      <div class="row">
        <div class="col-md-10 col-sm-10 col-xs-10">
          <p class="p-body1 q-mt-sm">OTHER LINES</p>
        </div>
      </div>

      <div class="row" style="margin-top: 15px; min-height: 50px">
        <div class="col-md-10" style="display: inherit">
          <line-number Line="201" Color="#D41217" class="q-mr-md q-mb-sm" />
          <line-number Line="202" Color="#31B5A4" class="q-mr-md q-mb-sm" />
          <line-number Line="203" Color="#6A509D" class="q-mr-md q-mb-sm" />
          <line-number Line="204" Color="#EBB500" class="q-mr-md q-mb-sm" />
          <line-number Line="211" Color="#21B9E6" class="q-mr-md q-mb-sm" />
          <line-number Line="212" Color="#F07E12" class="q-mr-md q-mb-sm" />
        </div>
      
      </div>

      <div class="row" style="margin-top: -20px; min-height: 50px">
        <div class="col-md-10" style="display: inherit">
          <line-number Line="201" Color="#D41217" class="q-mr-md q-mb-sm" />
          <line-number Line="202" Color="#31B5A4" class="q-mr-md q-mb-sm" />
          <line-number Line="203" Color="#6A509D" class="q-mr-md q-mb-sm" />
          <line-number Line="204" Color="#EBB500" class="q-mr-md q-mb-sm" />
          <line-number Line="211" Color="#21B9E6" class="q-mr-md q-mb-sm" />
          <line-number Line="212" Color="#F07E12" class="q-mr-md q-mb-sm" />
        </div>
        <hr class="separator" />
      </div>
      <div class="q-pa-md" style="text-align: center; margin-top: -10px;">
        <input type="button" class="btnmap" value="See map" />
      </div>
    </q-card-section>
  </q-card>
</template>

<script>
import { defineComponent } from "@vue/composition-api";
import LineNumber from "./LineNumber.vue";
import { Icon } from '@iconify/vue';

export default defineComponent({
  components: { LineNumber,Icon },
  props: {
    FirstStop: String,
    LastStop: String,
    Line: String,
    Color: String,
  },
  setup() {},
  computed: {
    style() {
      return "color: " + this.Color + ";";
    },
  },
});
</script>

<style scoped>
.p-body1 {
  color: #282828;
  font-weight: 600;
}

.btnmap {
  background: #282828;
  border-radius: 8px;
  width: 180px;
  height: 36px;
  font-family: Source Sans Pro;
  font-style: normal;
  font-weight: 600;
  font-size: 16px;
  line-height: 20px;

  /* Neutral (Dark)/00 */

  color: #ffffff;
}
.btnmap:hover{
  box-shadow: 0px 16px 16px -8px rgba(17, 17, 17, 0.25);
  background: #000000;
}

h4 {
  font-family: Source Sans Pro;
  font-style: normal;
  font-weight: bold;
  font-size: 21px;
  line-height: 140%;
  color: #282828;
}

label {
  font-family: Source Sans Pro;
  font-style: normal;
  font-weight: normal;
  font-size: 12px;
  line-height: 15px;
}

.p-body2 {
  color: #686868;
}

.provisional {
  border: 1px dashed #e6e6e6;
}
.separator {
  width: 20%;
  height: 4px;
  border: none;
  background: #e6e6e6;
  margin: 0 auto;
  border-radius: 8px;
  text-align: center;
  margin: 16px auto;
}
</style>
