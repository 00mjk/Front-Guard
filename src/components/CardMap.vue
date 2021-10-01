<template>
  <q-card class="my-card">
    <q-card-section   class="headercardmap"  >
      <img src="../assets/BusStop.svg" />
     
      <p  style="display:inline;color: #FFFFFF;" class="p-body1">{{Header}} </p>
    </q-card-section>
    <q-card-section>
      <p class="p-body2" style="font-size: 12px; color: #282828;">NEXT STOP</p>
    </q-card-section>
  </q-card>
</template>

<script>
import { defineComponent } from "@vue/composition-api";

export default defineComponent({
    props: {
      Header: String ,
      
      
  },
  setup() {},
});
</script>

<style scoped>
 .headercardmap{
  
height: 48px;


/* Bus Lines/201 */

background: #D41217;
/* Shadow/Soft */

box-shadow: 0px 8px 16px rgba(17, 17, 17, 0.04);
border-radius: 12px 12px 0px 0px;


/* Bus Lines/201 */

background: #D41217;
/* Shadow/Soft */

box-shadow: 0px 8px 16px rgba(17, 17, 17, 0.04);
border-radius: 12px 12px 0px 0px;
 }
</style>
