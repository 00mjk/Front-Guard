<template>
  <q-timeline color="green" style="margin-top: 158px">
    <q-timeline-entry class="raya"> </q-timeline-entry>

    <q-timeline-entry title="Hauptbahnhof " v-on:click="click(0)">
      <div class="contenido" id="0" style="display: none">
        <card-map Header="Imperial" />
      </div>
    </q-timeline-entry>
    <q-timeline-entry title="ZOB Bussteig 3"   v-on:click="click(1)">
      <div class="contenido" id="1" style="display: none">
        <card-map Header="Imperial" />
      </div>
    </q-timeline-entry>
    <q-timeline-entry title="Imperial" v-on:click="click(2)">
      <div class="contenido" id="2" style="display: none">
        <card-map Header="Imperial" />
      </div>
    </q-timeline-entry>
    <q-timeline-entry title="Kaufhof" v-on:click="click(3)">
      <div class="contenido" id="3" style="display: none">
        <card-map Header="Imperial" />
      </div>
    </q-timeline-entry>
    <q-timeline-entry title="Kunstmuseum" v-on:click="click(4)">
      <div class="contenido" id="4" style="display: none">
        <card-map Header="Imperial" />
      </div>
    </q-timeline-entry>
    <q-timeline-entry title="Köhlerbergstraße" v-on:click="click(5)">
      <div class="contenido" id="5" style="display: none">
        <card-map Header="Imperial" />
      </div>
    </q-timeline-entry>
    <q-timeline-entry title="VW-Bad" v-on:click="click(6)">
      <div class="contenido" id="6" style="display: none">
        <card-map Header="Imperial" />
      </div>
    </q-timeline-entry>
    <q-timeline-entry title="Emmausheim" v-on:click="click(7)">
      <div class="contenido" id="7" style="display: none">
        <card-map Header="Imperial" />
      </div>
    </q-timeline-entry>
    <q-timeline-entry title="Steimker Berg" v-on:click="click(8)">
      <div class="contenido" id="8" style="display: none">
        <card-map Header="Imperial" />
      </div>
    </q-timeline-entry>
    <q-timeline-entry title="Steimker Gärten" v-on:click="click(9)">
      <div class="contenido" id="9" style="display: none">
        <card-map Header="Imperial" />
      </div>
    </q-timeline-entry>
    <q-timeline-entry title="Nordsteimke" v-on:click="click(10)">
      <div class="contenido" id="10" style="display: none">
        <card-map Header="Imperial" />
      </div>
    </q-timeline-entry>
    <q-timeline-entry title="Nordsteimke, Kalkbergweg" v-on:click="click(11)">
      <div class="contenido" id="11" style="display: none">
        <card-map Header="Imperial" />
      </div>
    </q-timeline-entry>
    <q-timeline-entry title="Nordsteimke, Hohe Eichen" v-on:click="click(12)">
      <div class="contenido" id="12" style="display: none">
        <card-map Header="Imperial" />
      </div>
    </q-timeline-entry>
    <q-timeline-entry title="Barnstorf, Scharenhop" v-on:click="click(13)">
      <div class="contenido" id="13" style="display: none">
        <card-map Header="Imperial" />
      </div>
    </q-timeline-entry>
    <q-timeline-entry title="Barnstorf, Ringstraße" v-on:click="click(14)">
      <div class="contenido" id="14" style="display: none">
        <card-map Header="Imperial" />
      </div>
    </q-timeline-entry>
    <q-timeline-entry title="Barnstorf" v-on:click="click(15)">
      <div class="contenido" id="15" style="display: none">
        <card-map Header="Imperial" />
      </div>
    </q-timeline-entry>
    <q-timeline-entry
      title="Heiligendorf, Barnstorfer Straße"
      v-on:click="click(16)"
    >
      <div class="contenido" id="16" style="display: none">
        <card-map Header="Imperial" />
      </div>
    </q-timeline-entry>
    <q-timeline-entry title="Heiligendorf" v-on:click="click(17)">
      <div class="contenido" id="17" style="display: none">
        <card-map Header="Imperial" />
      </div>
    </q-timeline-entry>
    <q-timeline-entry title="Heiligendorf, Grüner Jäger" v-on:click="click(18)">
      <div class="contenido" id="18" style="display: none">
        <card-map Header="Imperial" />
      </div>
    </q-timeline-entry>
    <q-timeline-entry title="Heiligendorf, Hasenmorgen" v-on:click="click(19)">
      <div class="contenido" id="19" style="display: none">
        <card-map Header="Imperial" />
      </div>
    </q-timeline-entry>
    <q-timeline-entry title="Neindorf, Bahnhof" v-on:click="click(20)">
      <div class="contenido" id="20" style="display: none">
        <card-map Header="Imperial" />
      </div>
    </q-timeline-entry>
    <q-timeline-entry title="Neindorf" v-on:click="click(21)">
      <div class="contenido" id="21" style="display: none">
        <card-map Header="Imperial" />
      </div>
    </q-timeline-entry>
  </q-timeline>
</template>
<script>
/*Cambiar los argumentos de los eventos click por $event , y realizar los cambios oportunos en el codigo */

import { defineComponent } from "@vue/composition-api";
import CardMap from "./CardMap.vue";

export default defineComponent({
  components: { CardMap },
  setup() {},
  methods: {
    click: function (id) {
      click(id);

      function click(elemento) {
        if (
          document.getElementsByClassName("contenido")[elemento].style
            .display == "none"
        ) {
          document.getElementsByClassName("contenido")[elemento].style.display =
            "block";
        } else {
          document.getElementsByClassName("contenido")[elemento].style.display =
            "none";
        }
      }
    },
  },
});
</script>

<style scoped>
.lista {
  background-color: darkgreen;
}
</style>

<style>
ul::after {
  border: 3px solid transparent !important;
  background: rgb(49, 168, 54) !important;
}

.q-timeline__dot::before {
  background: white !important;
  border: 3px solid !important;
}
.q-timeline__dot::after {
  margin-top: -5px;
  margin-bottom: -13px;
  width: 4px;
  opacity: 1;
}
.q-timeline__entry:nth-child(2) .q-timeline__dot::before {
  border: 3px solid transparent !important;
  background: rgb(49, 168, 54) !important;
}

.q-timeline__entry:last-child .q-timeline__dot::before {
  border: 3px solid transparent !important;
  background: rgb(49, 168, 54) !important;
}

.q-timeline__entry:last-child .q-timeline__dot::after {
  margin-top: -5px !important;
margin-bottom: 10px !important;
width: 4px !important;
opacity: 1 !important;
content: "";
   background: rgb(49, 168, 54) !important;
}

.raya .q-timeline__dot::before {
  display: none;
}
.raya .q-timeline__dot::after {
  margin-top: -158px;
}
</style>
