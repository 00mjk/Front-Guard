<template >
  <div  id="home" style="position: relative;width: 1920px;height: 5573px;">
 <header class="header">
   <img src="../assets/Logo.svg" class="imagencabecera">

   <div id="right-side" style="position: absolute;width: 80px;height: 26px;left: 1229px;top: 48px;">
       <img src="../assets/cil_language.svg" class="lenguajecabecera"> 
       <img src="../assets/mdi_checkbox-blank-badge-outline.svg" class="checkboxcabecera">  
  </div>

  <div  id="div-cabecera" class="divcabecera">
   <img src="../assets/mdi_menu.png" class="menucabecera">  
  </div>

 </header>

 <nav>
<ul style="list-style:none">

    <li  class="navcabecera" ><a class="subnavcabecera"  href="/es/">HOME</a></li>


  </ul>
   </nav>

 
 </div>
</template>

<script>
import { ref } from 'vue'


export default {
  setup () {
    const leftDrawerOpen = ref(false)
    const rightDrawerOpen = ref(false)

    return {
      leftDrawerOpen,
      toggleLeftDrawer () {
        leftDrawerOpen.value = !leftDrawerOpen.value
      },

      rightDrawerOpen,
      toggleRightDrawer () {
        rightDrawerOpen.value = !rightDrawerOpen.value
      }
    }
  }
}
</script>
