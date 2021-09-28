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
          <q-breadcrumbs-el label="HOME" />
        </q-breadcrumbs>
      </div>
    </div>

    <div class="row q-col-gutter-md">
      <div class="col-md-6 col-sm-12">
        <h4>Welcome Fahrgast!</h4>
        <h1 class="saludo">
          Where are you <span style="color: #d92127">going?</span>
        </h1>
      </div>

      <div class="col-md-6 col-sm-12">
        <img src="../assets/wolfsburg-hero.png" class="max-width100" />
      </div>
    </div>

    <div class="row q-col-gutter-md">
      <div class="col-md-8"></div>

      <div class="col-md-4 col-sm-12">
        <div class="cardalert">
          <div class="q-pa-md">
            <q-carousel
              v-model="slide"
              swipeable
              animated
              :control-type="controlType"
              control-color="dark"
              navigation
              padding
              arrows
              height="190px"
              class="text-purple rounded-borders"
            >
              <q-carousel-slide name="style" class="column no-wrap flex-center">
                <q-icon name="style" size="36px" />
                <div class="q-mt-md text-center text-black">Slider1</div>
              </q-carousel-slide>
              <q-carousel-slide name="tv" class="column no-wrap flex-center">
                <q-icon class="left:true;" name="live_tv" size="56px" />
                <div class="q-mt-md text-center text-black">Slider2</div>
              </q-carousel-slide>
              <q-carousel-slide
                name="layers"
                class="column no-wrap flex-center"
              >
                <q-icon name="layers" size="56px" />
                <div class="q-mt-md text-center text-black">Slider3</div>
              </q-carousel-slide>
              <q-carousel-slide name="map" class="column no-wrap flex-center">
                <q-icon name="terrain" size="56px" />
                <div class="q-mt-md text-center text-black">Slider4</div>
              </q-carousel-slide>
            </q-carousel>
          </div>
        </div>
      </div>
    </div>

    <form>
      <div class="row q-col-gutter-md">
        <div class="col-md-2 col-sm-6">
          <h4>Trip planner<span style="color: #d92127">.</span></h4>
          <p style="font-size: 14px">Routes from Monday to Saturday</p>
        </div>
      </div>

      <div class="row q-col-gutter-md">
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

      <div class="row q-col-gutter-md">
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
          <input type="button" class="btnsubmit" value="Plan My trip" />
        </div>
      </div>
    </form>

    <hr class="hrstyle" />

    <form>
      <div class="row q-col-gutter-md">
        <div class="col-md-2 col-sm-6">
          <h4>Bus lines info<span style="color: #d92127">.</span></h4>
          <p style="font-size: 14px">Routes from Monday to Saturday</p>
        </div>
      </div>

      <div class="row q-col-gutter-md">
        <div class="col-md-8 col-sm-12">
          <div class="q-pa-md">
            <search-input Header="Label" />
          </div>
          <div class="busCards">
          <bus-card
            Color="blue"
            Numero="201"
            Label1="Velstove"
            Label2="Mörser Winkel"
          />
          <bus-card
            Color="pink"
            Numero="201"
            Label1="Velstove"
            Label2="Mörser Winkel"
          />
          <bus-card
            Color="pink"
            Numero="201"
            Label1="Velstove"
            Label2="Mörser Winkel"
          />
          <bus-card
            Color="pink"
            Numero="201"
            Label1="Velstove"
            Label2="Mörser Winkel"
          />
          <bus-card
            Color="pink"
            Numero="201"
            Label1="Velstove"
            Label2="Mörser Winkel"
          />
          <bus-card
            Color="pink"
            Numero="201"
            Label1="Velstove"
            Label2="Mörser Winkel"
          />
          <bus-card
            Color="pink"
            Numero="201"
            Label1="Velstove"
            Label2="Mörser Winkel"
          />
          <bus-card
            Color="pink"
            Numero="201"
            Label1="Velstove"
            Label2="Mörser Winkel"
          />
          <bus-card
            Color="pink"
            Numero="201"
            Label1="Velstove"
            Label2="Mörser Winkel"
          />
          <bus-card
            Color="pink"
            Numero="201"
            Label1="Velstove"
            Label2="Mörser Winkel"
          />
          </div>
        </div>

        <div class="col-md-4 col-sm-12">
          <div class="q-card my-card">
           
              <google-maps />
            
          </div>
        </div>
      </div>
    </form>
  </q-page>
</template>

<script>
import { ref } from "vue";
import InputGenericoHome from "src/components/InputGenericoHome.vue";
import DateInput from "src/components/DateInputOn.vue";
import TimeInput from "src/components/TimeInput.vue";
import SearchInput from "src/components/SearchInput.vue";
import BusCard from "src/components/BusCard.vue";
import GoogleMaps from "src/components/GoogleMaps.vue";

export default {
  components: {
    InputGenericoHome,
    DateInput,
    TimeInput,
    SearchInput,
    BusCard,
    GoogleMaps,
  },
  setup() {
    return {
      search: ref(""),
      model: ref("one"),
      secondModel: ref("one"),
      controlType: ref("flat"),
      controlTypeOptions: [
        { value: "regular", label: "regular" },
        { value: "unelevated", label: "unelevated" },
        { value: "flat", label: "flat (default)" },
        { value: "outline", label: "outline" },
        { value: "push", label: "push" },
      ],

      slide: ref("style"),
      lorem: "Failure of the passenger information display ",
    };
  },
};
</script>

<style lang="sass" scoped>
.my-custom-toggle
  border: 1px solid #027be3
</style>
