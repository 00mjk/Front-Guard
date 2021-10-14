<template>
  <q-timeline color="green" style="margin-top: 150px">
    <q-timeline-entry title="Hauptbahnhof" v-on:click="click(0)">
      <div class="contenido" id="0" style="display: none">
        <card-map Header="Imperial" />
      </div>
    </q-timeline-entry>

    <q-timeline-entry title="ZOB Bussteig 3" v-on:click="click(1)">
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
  </q-timeline>
</template>
<script>
import { defineComponent } from "@vue/composition-api";
import CardMap from "./CardMap.vue";

export default defineComponent({
  components: { CardMap },
  setup() {},
  methods: {
    click: function (id) {
      click(id);

    

      function click(elemento) {
        console.log("click");

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
        console.log(
          document.getElementsByClassName("contenido")[elemento].style.display
        );
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
