<template>
  <q-card class="my-card" style=" width: 100%;">
    <div class="q-pa-md" style="display:flex;">
      <div class="container"  style="width: 100%;">
        <q-card-section style="padding: 0 0 0 8px">
          <div class="text-p q-mb-xs">{{ Header }}</div>
        </q-card-section>
        <div class="q-gutter-y-md column">
          <q-input 
            
            filled
            clearable
            color="dark"
            label="Label2"
           
           
          >
          </q-input>
        </div>


         <q-card-section style="padding: 0 0 0 8px">
         <q-toggle class="p-body2 q-mr-xl"
        v-model="value"
        color="red"
        label="DayTime bus lines"
        left-label size="xs"
      />
      <q-toggle class="p-body2 q-mr-xl"
        v-model="value1"
        color="red"
        label="Evening bus lines"
        left-label size="xs"
      />
      <q-toggle class="p-body2 q-mr-xl"
        v-model="value2"
        color="red"
        label="Special lines"
        left-label size="xs"
      />
        </q-card-section>
      </div>

      <div  >
        <input type="button" class="btnsubmit" value="Search"  style="margin-top: 25px;" />
      </div>
    </div>
  </q-card>
</template>

<script>
import { event } from "quasar";
import { ref, computed } from "vue";

const { stopAndPrevent } = event;

export default {
  props: {
    Header: String,
    Hint: String,
    Label: String,
  },
  computed: {
    showHeader: function () {
      return this.Header;
    },
    showHint: function () {
      return this.Hint;
    },

    showLabel: function () {
      return this.Label;
    },
  },
  setup() {
    return{
      value: ref(false),
       value1: ref(false),
       value2: ref(false),
       
    }
    
    
    
  },
};
</script>
