<template>
  <q-layout id="home">
    <q-header class="bg-primary text-white">
      <q-toolbar style="height: 120px">
        <q-toolbar-title class="text-center">
          <a href="./">
            <img
              id="transicion1"
              class="transicion1"
              src="../assets/Logo.svg"
              style="width: 35.09px; height: 50px"
          /></a>
        </q-toolbar-title>
        <div class="header-icons">
          <a> <img src="../assets/cil_language.svg" /></a>
          <a> <img src="../assets/mdi_checkbox-blank-badge-outline.svg" /> </a>
          <a> <img src="../assets/mdi_menu.png" class="menucabecera" /> </a>
        </div>
      </q-toolbar>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>

    <footer class="footer" style="margin-top: 315px">
      <div class="row q-col-gutter-md" style="margin-bottom: 72px">
        <div class="col-md-2 col-sm-6">
          <img src="../assets/WVGLogo.svg" />
          <div>
            <div
              class="direction"
              style="margin-bottom: 24px; margin-top: 24px"
            >
              <p class="texto1footer">Wolfsburger Verkehrs-GmbH</p>
              <p class="texto2footer">
                Borsigstraße 28 <br />
                38446 Wolfsburg
              </p>
            </div>
          </div>

          <div class="contact" style="margin-bottom: 24px">
            <p class="p-body2">
              Telefon: 05361 189 8888 <br>
              <a
                style="text-decoration: none; color: #282828"
                href="info@wvg.de"
                >info@wvg.de
              </a>
            </p>
          </div>

          <div style="margin-bottom: 74px">
            <a target="_blank" href="https://www.facebook.com/wvg.wolfsburg/">
              <img
                src="../assets/mdi_facebook.svg"
                style="margin-right: 28px"
              />
            </a>
            <a
              target="_blank"
              href="https://www.youtube.com/channel/UCHiMdeVeUprCOvN7nE_mnFQ"
              ><img
                src="../assets/mdi_youtube.svg"
                style="margin-right: 28px"
              />
            </a>
            <a
              target="_blank"
              href="https://www.instagram.com/stadtwerkewolfsburg/?hl=de"
            >
              <img src="../assets/mdi_instagram.svg" />
            </a>
          </div>

          <p class="textohotline">Service Hotline</p>
          <p class="numerohotline">05361 189 8888</p>
        </div>
      </div>
      <hr class="hrstyle" />
      <p class="copycredits">© 2021 Wolfsburger Verkehrs-GmbH</p>
    </footer>
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
