<template>
  <q-card class="my-card" style="min-height: 309px;">
    <q-card-section class="headercardmap">
      <img src="../assets/BusStop.svg" />
        
      <p style=" color: #ffffff; display:inline;" class="p-body1">
        {{ Header }}
      </p>
    </q-card-section>
    <q-card-section>
      <p class="p-body2" style="color: #282828">NEXT STOP</p>
      <p
        class="p-body1"
        style="color: #282828; margin-top: 7px; margin-bottom: 16px"
      >
        Hattorfer Str.
      </p>
      <label style="color: #282828">OCCUPANCY</label><br />
      <label style="color: #282828">TRANSFER</label>
    </q-card-section>
  </q-card>
</template>

<script>
import { defineComponent } from "@vue/composition-api";

export default defineComponent({
  props: {
    Header: String,
    NextStop: String,
    Occupancy: String,
    Transfer: String,
  },
  setup() {},
});
</script>

<style scoped>
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
</style>
