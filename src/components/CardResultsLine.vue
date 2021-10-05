<template>
  <div :v-if="Type == 'Walk'">
    <div class="q-px-md">
      <div class="row">
        <div class="col-md-2 col-sm-2">
          <div style="display: inline">
            <legend style="margin-top: 5px">12:20</legend>
          </div>
        </div>

        <div class="col-md-2 col-sm-2 center">
          <img class="moneco" src="../assets/Walk.svg" />
        </div>

        <div class="col-md-8 col-sm-2">
          <label> {{BusStop}}</label>
        </div>
      </div>

      <div class="row">
        <div class="col-md-2 col-sm-2"></div>

        <div class="col-md-2 col-sm-2 center q-mt-sm">
          <img src="../assets/Line215.svg" class="moneco" />
        </div>

        <div class="col-md-8 col-sm-2">
          <legend>{{Distance}} m</legend>
          <legend>about {{Time}} minutes</legend>
        </div>
      </div>
    </div>
  </div>
  <div :v-else-if="Type == 'Line'">
    <div :v-if="Type == 'Walk'">
      <div class="q-px-md">
        <div class="row">
          <div class="col-md-2 col-sm-2">
            <div style="display: inline">
              <legend style="margin-top: 5px">12:20</legend>
            </div>
          </div>

          <div class="col-md-2 col-sm-2 center">
            <div class="box moneco" :style="style" >
              <p class="numero">212</p>
            </div>
          </div>

          <div class="col-md-8 col-sm-2">
            <label>{{BusStop}}</label>
          </div>
        </div>

        <div class="row">
          <div class="col-md-2 col-sm-2"></div>

          <div class="col-md-2 col-sm-2 center q-mt-sm">
            <img src="../assets/Line215.svg" class="moneco" />
          </div>

          <div class="col-md-8 col-sm-2">
            <legend>{{BusStops}} bus stops</legend>
            <legend> {{Time}} minutes</legend>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { defineComponent } from "@vue/composition-api";

export default defineComponent({
  props: {
    Type: String,
    Distance: String,
    Time: String,
    Line: String,
    Color: String,
    BusStop: String,
    BusStops: String,
  },
  computed: {
    style() {
      return "background: " + this.Color + ";";
    },
  },

  setup() {
    return {};
  },
});
</script>
