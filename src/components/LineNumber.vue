<template>
  <div class="box " :style="style">
    <p class="numero">{{ Line }}</p>
  </div>
</template>

<script>
import { defineComponent } from "@vue/composition-api";

export default defineComponent({
  props: {
      Color: String,
      Line: String,

  },
  setup() {},
  computed: {
    style() {
      return "background: " + this.Color + ";";
    },
  },
});
</script>

<style scoped>
.box {
  background: #f07e12;
 width: 40px;
height: 20px;
  
  text-align: center;
  justify-content: center;

  box-shadow: 0px 8px 16px rgba(17, 17, 17, 0.04);
border-radius: 16px;
}

.box p{
    height: 100%;
    text-align: center;
justify-content: center;
display: flex;


}


.numero {
  font-family: Source Sans Pro;
  font-style: normal;
  font-weight: bold;
  font-size: 13px;
  line-height: 16px;
  display: flex;
  align-items: center;
  text-align: center;
  letter-spacing: 0.03em;
  

  /* Neutral (Dark)/00 */

  color: #ffffff;
}



</style>
