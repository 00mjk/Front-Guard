<template>
  <q-layout id="home">
    <q-header class="bg-primary text-white">
      <q-toolbar style="height: 120px; border: 1px solid black">
        <q-toolbar-title class="text-center" style="border: 1px solid black">
          <img src="../assets/Logo.svg" style="width: 35.09px; height: 50px" />
        </q-toolbar-title>
        <div class="header-icons">
          <img src="../assets/cil_language.svg" />
          <img src="../assets/mdi_checkbox-blank-badge-outline.svg" />
          <img src="../assets/mdi_menu.png" class="menucabecera" />
        </div>
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>

    <q-footer class="footer">
      <img src="../assets/WVGLogo.svg" class="logofooter" />
      <div
        style="
          position: absolute;
          width: 220px;
          height: 60px;
          left: 0px;
          top: 87px;
        "
      >
        <p class="texto1footer">Wolfsburger Verkehrs-GmbH</p>
        <p class="texto2footer">
          Borsigstraße 28 <br />
          38446 Wolfsburg
        </p>
      </div>

      <div>
        <p
          class="informacioncontactofooter"
          style="
            position: absolute;
            width: 220px;
            height: 36px;
            left: 0px;
            top: 171px;
            color: #282828;
          "
        >
          Telefon: 05361 189 8888 <br />
          <a style="text-decoration: none; color: #282828" href="info@wvg.de"
            >info@wvg.de
          </a>
        </p>
      </div>

      <div class="divsocialfooter">
        <a target="_blank" href="https://www.facebook.com/wvg.wolfsburg/">
          <img
            src="../assets/mdi_facebook.svg"
            style="position: absolute; width: 24px; height: 24px; left: 0px"
            class="logofooter"
          />
        </a>
        <a
          target="_blank"
          href="https://www.youtube.com/channel/UCHiMdeVeUprCOvN7nE_mnFQ"
          ><img
            src="../assets/mdi_youtube.svg"
            style="position: relative; width: 24px; height: 24px; left: 48px"
            class="logofooter"
          />
        </a>
        <a
          target="_blank"
          href="https://www.instagram.com/stadtwerkewolfsburg/?hl=de"
        >
          <img
            src="../assets/mdi_instagram.svg"
            style="position: absolute; width: 24px; height: 24px; left: 96px"
            class="logofooter"
          />
        </a>
      </div>

      <div class="divhotline">
        <p class="textohotline">Service Hotline</p>
        <p class="numerohotline">05361 189 8888</p>
      </div>

      <div class="divcredits">
        <hr />
        <p class="copycredits">© 2021 Wolfsburger Verkehrs-GmbH</p>
      </div>
    </q-footer>
  </q-layout>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    const leftDrawerOpen = ref(false);
    const rightDrawerOpen = ref(false);

    return {
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },

      rightDrawerOpen,
      toggleRightDrawer() {
        rightDrawerOpen.value = !rightDrawerOpen.value;
      },
    };
  },
};
</script>
