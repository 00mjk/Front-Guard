<template>
  <div class="cardbus">
    <div class="container">
      <div class="header">
        <div id="style" :style="style"  class="color">
          <p style="color: #ffffff">{{ Numero }}</p>
        </div>
      </div>
      <hr class="separator" />

      <div class="text">
        <p>{{ Label1 }}</p>

        <p>{{ Label2 }}</p>
      </div>
    </div>
  </div>
</template>

<script>
import { defineComponent } from "@vue/composition-api";

export default defineComponent({
  props: {
    Numero: String,
    Label1: String,
    Label2: String,
    Color: String,
  },
  computed: {
    style() {
      return (
        "background: " +
        this.Color +
        ";"
      );
    },

    hoverstyle: function(){
      return(
        "--borderHover: 1px solid " + this.Color 
      );
    },
  },

  setup() {
    return {};
  },
});
</script>
  


<style scoped>
.cardbus .header .color {
  text-align: center;
  justify-content: center;
  align-items: center;
  width: auto;
  height: 60px;
  border-radius: 16px;
  display: flex;
}

.cardbus .separator {
  display: inline-block;
  width: 30%;
  height: 3px;
  border: none;
  background: #e6e6e6;
  margin: 0 auto;
  border-radius: 8px;
  text-align: center;
  margin: 16px auto;
}

.cardbus:hover {
  border: 1px solid ;
  box-sizing: border-box;
  box-shadow: 0px 15px 32px -16px rgba(212, 18, 23, 0.35);
  border-radius: 24p;
}
.cardbus .header {
  width: 100%;
}

.cardbus p {
  font-family: Source Sans Pro;
  font-style: normal;
  font-weight: normal;
  font-size: 14px;
  line-height: 140%;
  color: #282828;
  padding-top: 8px;
}

.cardbus .container {
  padding: 16px;
  display: flex;
  flex-wrap: wrap;
}

.cardbus {
 width: calc(100%/5 - 19px);
height: 192px;
background: #ffffff;
box-shadow: 0px 15px 32px -16px rgba(17, 17, 17, 0.06);
border-radius: 24px;
display: inline-block;
margin: 16px 16px 0 0;
border: 1px solid white;
}

.cardbus .text {
  text-align: left;
  width: 100%;
}
</style>
