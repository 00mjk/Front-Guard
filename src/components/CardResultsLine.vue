<template>
  <div v-if="Walk">
    <div class="q-px-md">
      <div class="row">
        <div class="col-md-2 col-sm-2">
          <div style="display: inline">
            <legend style="margin-top: 5px">{{ Hour }}</legend>
          </div>
        </div>

        <div class="col-md-2 col-sm-2 center">
          <img class="moneco" src="../assets/Walk.svg" />
        </div>

        <div class="col-md-8 col-sm-2">
          <label> {{ BusStop }}</label>
        </div>
      </div>

      <div class="row">
        <div class="col-md-2 col-sm-2"></div>

        <div class="col-md-2 col-sm-2 center q-mt-sm">
          <img src="../assets/Line215.svg" class="moneco" />
        </div>

        <div class="col-md-8 col-sm-2">
          <legend>{{ Distance }} m</legend>
          <legend>about {{ Time }} minutes</legend>
        </div>
      </div>
    </div>
  </div>
  <div v-else>
    <div v-if="!Walk && !Final">
      <div class="q-px-md">
        <div class="row">
          <div class="col-md-2 col-sm-2">
            <div style="display: inline">
              <legend style="margin-top: 5px">{{ Hour }}</legend>
            </div>
          </div>

          <div class="col-md-2 col-sm-2 center">
            <div class="box moneco" :style="style">
              <p class="numero">{{ Line }}</p>
            </div>
          </div>

          <div class="col-md-8 col-sm-2">
            <label>{{ BusStop }}</label>
          </div>
        </div>

        <div class="row">
          <div class="col-md-2 col-sm-2" ></div>

          <div class="col-md-2 col-sm-2 center q-mt-sm col-line" style="margin-top: -2px;">
            
          </div>

          <div class="col-md-8 col-sm-2">
            <legend>{{ BusStops }} bus stops</legend>
            <legend>{{ Time }} minutes</legend>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div v-if="Final">
    <div class="q-px-md">
      <div class="row">
        <div class="col-md-2 col-sm-2">
          <div style="display: inline">
            <legend style="margin-top: 5px">{{ Hour }}</legend>
          </div>
        </div>

        <div class="col-md-2 col-sm-2 center ">
          <img src="../assets/Final.svg" class="moneco" />
        </div>

        <div class="col-md-8 col-sm-2">
          <label>{{ BusStop }}</label>
        </div>
      </div>

      <div class="row">
        <div class="col-md-2 col-sm-2"></div>

        <div class="col-md-2 col-sm-2 center "></div>

        <div class="col-md-8 col-sm-2"></div>
      </div>
    </div>
  </div>
</template>

<style scoped>

.col-line::before {
content: "";
display: inline-block;
height: 55px;

border: 2px solid #D41217;
}
</style>

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
    Walk: Boolean,
    Number: Number,
    Hour: String,
    Final: Boolean,
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
