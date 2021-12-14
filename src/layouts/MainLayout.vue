<template>
    <q-layout id="home">
        <q-header class="bg-primary text-white">
            <q-toolbar>
                <q-toolbar-title class="text-center q-pa-none">
                    <a href="./"> <img id="transicion1" class="transicion1" src="../assets/Logo.svg" /></a>
                </q-toolbar-title>
                <div class="header-icons">
                    <a href="#"> <img src="../assets/cil_language.svg" /></a>
                    <a href="#"> <img src="../assets/mdi_checkbox-blank-badge-outline.svg" /> </a>
                    <q-btn size="16px" flat round @click="$q.dark.toggle()" :icon="$q.dark.isActive ? 'nights_stay' : 'wb_sunny'"/>
                    <a class="menucabecera" href="#">
                        <svg  :onclick="openNav" width="24" height="40" viewBox="0 0 24 40" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <g clip-path="url(#clip0_1693:1640)">
                                <path d="M18 5L18 35L17 35L17 5L18 5ZM13 5L13 35L12 35L12 5L13 5ZM8 5L8 35L7 35L7 5L8 5Z" fill="#282828" />
                            </g>
                            <defs>
                                <clipPath id="clip0_1693:1640">
                                    <rect width="40" height="24" fill="white" transform="translate(24) rotate(90)" />
                                </clipPath>
                            </defs>
                        </svg>
                    </a>
                </div>
            </q-toolbar>
        </q-header>
        <div id="myNav" class="overlay">
            <a href="javascript:void(0)" class="closebtn" :onclick="closeNav">&times;</a>
            <div class="overlay-content">
                <a href="#">About</a>
                <a href="#">Services</a>
                <a href="#">Clients</a>
                <a href="#">Contact</a>
            </div>
        </div>

        <q-page-container>
            <router-view />
        </q-page-container>

        <footer class="footer">
            <div class="row info-footer">
                <div class="col-md-12 col-sm-12">
                    <div class="logo-footer q-mb-lg">
                        <img src="../assets/WVGLogo.svg" />
                    </div>
                    <div class="direction q-mb-md">
                        <p class="texto1footer">Wolfsburger Verkehrs-GmbH</p>
                        <p class="texto2footer">
                            Borsigstraße 28 <br />
                            38446 Wolfsburg
                        </p>
                    </div>

                    <div class="contact q-mb-lg">
                        <p class="p-body2">Telefon: 05361 189 8888</p>
                        <p class="p-body2">
                            <a href="info@wvg.de">info@wvg.de </a>
                        </p>
                    </div>

                    <div class="social-footer">
                        <a target="_blank" href="https://www.facebook.com/wvg.wolfsburg/">
                            <span class="iconify" data-icon="mdi:facebook" data-height="24"></span>
                        </a>
                        <a target="_blank" href="https://www.youtube.com/channel/UCHiMdeVeUprCOvN7nE_mnFQ">
                            <span class="iconify" data-icon="mdi:youtube" data-height="24"></span>
                        </a>
                        <a target="_blank" href="https://www.instagram.com/stadtwerkewolfsburg/?hl=de">
                            <span class="iconify" data-icon="mdi:instagram" data-height="24"></span>
                        </a>
                    </div>

                    <p class="textohotline q-pb-sm">Service Hotline</p>
                    <p class="numerohotline">05361 189 8888</p>
                </div>
            </div>
            <div class="row legal-footer">
                <div class="col-md-12 col-sm-12">
                    <p class="copycredits">© 2021 Wolfsburger Verkehrs-GmbH</p>
                </div>
            </div>
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
    methods:{
         openNav: function() {
  document.getElementById("myNav").style.width = "100%";
},

 closeNav: function() {
  document.getElementById("myNav").style.width = "0%";
}
    },
    
};


</script>

<style scoped lang="scss">

.overlay .closebtn {
  position: absolute;
  top: 20px;
  right: 45px;
  font-size: 60px;
}

@media screen and (max-height: 450px) {
  .overlay a {font-size: 20px}
  .overlay .closebtn {
  font-size: 40px;
  top: 15px;
  right: 35px;
  }
}

.overlay {
  height: 100%;
  width: 0;
  position: fixed;
  z-index: 2001;
  top: 0;
  left: 0;
  background-color: rgb(0,0,0);
  background-color: rgba(0,0,0, 0.9);
  overflow-x: hidden;
  transition: 0.5s;
}
.overlay-content {
  position: relative;
  top: 25%;
  width: 100%;
  text-align: center;
  margin-top: 30px;
}

.overlay a {
  padding: 8px;
  text-decoration: none;
  font-size: 36px;
  color: #818181;
  display: block;
  transition: 0.3s;
}


.overlay a:hover, .overlay a:focus {
  color: #f1f1f1;
}


/* START header */
.q-toolbar {
    max-width: 1440px;
    margin: 0px auto;
    padding: 0 16px;
    height: 120px;

    .q-toolbar__title {
        a {
            display: flex;
            width: 36px;
            margin: 0 auto;
        }
    }
}

.header-icons {
    position: absolute;
    right: 0;
    display: flex;
    padding-right: 16px;
    justify-content: space-between;
    margin: 0;

    a {
        display: flex;
        margin: 0 16px;
        transition: all 0.4s ease-in-out;

        img {
            padding: 0;
            max-width: 20px;
        }

        path {
            transition: all 0.4s ease-in-out;
        }

        &.menucabecera {
            margin-left: 50px;

            &:hover {
                transform: rotate(450deg);

                path {
                    fill: var(--main);
                }
            }
        }
    }
}

/* ----------------------------------- 680px */
@media (max-width: 680px) {
    .q-toolbar {
        height: 70px;
    }

    .header-icons {
        a {
            margin: 0 8px;

            img {
                max-width: 16px;
            }

            &.menucabecera {
                margin-left: 20px;
                margin-right: 0;
            }
        }
    }
}

/* FIN header */

/* START footer */
.footer {
    max-width: 1440px;
    margin: 300px auto 0;
    min-height: 0px;
    padding: 16px 16px 80px;

    .info-footer {
        padding-bottom: 72px;
        border-bottom: 1px solid var(--neutral-40);
        margin-bottom: 24px;

        .logo-footer {
            height: 63px;

            img {
                height: 63px;
                width: auto;
            }
        }

        .direction {
            p {
                padding-bottom: 8px;
            }
        }

        .contact {
            a {
                color: var(--neutral-80);

                &:hover {
                    color: var(--main);
                }
            }
        }

        .social-footer {
            display: flex;
            align-items: center;
            gap: 24px;
            margin-bottom: 72px;

            a {
                color: var(--neutral-40);
                &:hover {
                    color: var(--neutral-80);
                }
            }
        }
    }
}
/* END footer */
</style>
