<template>
  <q-card class="my-card">
    <div class="q-pa-md">
      <q-card-section style="padding: 0 0 0 8px">
        <div class="text-p q-mb-xs">{{ Header }}</div>
      </q-card-section>

      <div class="q-gutter-y-md column">
        <q-input v-model="time" filled type="time" >
          <template v-slot:append> </template>
        </q-input>
      </div>
    </div>
  </q-card>
</template>

<script>
import { ref } from "vue";

export default {
  props: {
    Header: String,

    Label: String,
  },
  setup() {
    return {
      time: ref(""),
    };
  },
};
</script>
