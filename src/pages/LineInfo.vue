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
          <a style="text-decoration: none" href="./">
            <q-breadcrumbs-el label="HOME / LINES / TRIP PLANNER" />
          </a>
        </q-breadcrumbs>
      </div>
    </div>
    <div class="row q-col-gutter-md" style="margin-top: 61px">
      <div class="col-md-2 col-sm-6 q-mb-lg">
        <h4>Line Info<span style="color: #d92127">.</span></h4>
        <p class="p-body2">Routes from Monday to Saturday</p>
      </div>
    </div>

    <div class="row q-col-gutter-md" style="margin-top: 24px">
      <div class="col-md-4">
        <line-info-card Color="#31A836" FirstStop="Hauptbahnhof" LastStop="Neindorf" Line="215"/>
        </div>
        <div class="col-md-8">
       
        </div>
    </div>


     <div class="row q-col-gutter-md " style="margin-top: 500px">
      <div class="col-md-6 col-sm-12">
        
        <h1 class="saludo">
          Where are you <span style="color: #d92127">going?</span>
        </h1>
      </div>
      </div>

      <form style="margin-bottom: 1050px">
      <div class="row q-col-gutter-md" style="margin-top: 61px">
        <div class="col-md-2 col-sm-6 q-mb-lg">
          <h4>Trip planner<span style="color: #d92127">.</span></h4>
          <p class="p-body2">Routes from Monday to Saturday</p>
        </div>
      </div>

      <div class="row q-col-gutter-md q-mb-xl">
        <div class="col-md-6 col-sm-12 col-xs-12">
          <q-card class="my-card">
            <input-generico-home
              Header="From"
              Hint="Write the name of the street, bus stop or activate your location"
              Label="Hola"
            />
          </q-card>
        </div>
        <div class="col-md-6 col-sm-12 col-xs-12">
          <q-card class="my-card">
            <input-generico-home
              Hint="Write the name of the street, bus stop or activate your location"
              Header="To"
            >
            </input-generico-home>
          </q-card>
        </div>
      </div>

      <div class="row q-col-gutter-md">
        <div class="col-md-2 col-sm-6">
          <p>I´D LIKE TO</p>
        </div>
      </div>

      <div class="row q-col-gutter-md q-mb-xl">
        <div class="col-md-6 col-sm-12 col-xs-12">
          <div class="radio-toolbar">
            <input
              type="radio"
              id="radioApple"
              name="radioFruit"
              value="DEPART"
              checked
            />
            <label for="radioApple">DEPART</label>

            <input
              type="radio"
              id="radioBanana"
              name="radioFruit"
              value="ARRIVE"
            />
            <label for="radioBanana">ARRIVE</label>

            <input
              type="radio"
              id="radioOrange"
              name="radioFruit"
              value="REGULAR JORNEY"
            />
            <label for="radioOrange">REGULAR JORNEY</label>
          </div>
        </div>

        <div class="col-md-3 col-sm-6 col-xs-12 q-pl-md">
          <time-input Header="To"> </time-input>
        </div>

        <div class="col-md-3 col-sm-6 col-xs-12 q-pl-md">
          <date-input Header="On" />
        </div>
      </div>

      <div class="row items-end">
        <div class="col-md-2">
          <input type="button" class="btnsubmit" onclick="location.href='../#/TripPlanner'" value="Plan My trip" />
        </div>
      </div>
    </form>
  </q-page>
</template>

<script>
import { defineComponent } from "@vue/composition-api";
import LineInfoCard from "src/components/LineInfoCard.vue";

import InputGenericoHome from "src/components/InputGenericoHome.vue";
import DateInput from "src/components/DateInputOn.vue";
import TimeInput from "src/components/TimeInput.vue";

export default defineComponent({
  components: { LineInfoCard,InputGenericoHome,
    DateInput,
    TimeInput },
  setup() {},
});
</script>

<style scoped></style>
