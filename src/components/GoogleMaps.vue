<template>
    <div class="mapa">
        <div class="q-pa-md">
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d11912.084941383731!2d10.801808852063795!3d52.426292973821795!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47af93c8d01e69e5%3A0xe2465df60ba210ae!2sVolkswagen-Arena!5e0!3m2!1ses!2ses!4v1632827773646!5m2!1ses!2ses" allowfullscreen="" loading="lazy" key="" style="min-height: 600px; border: 0; height: 100%; width: 100%"></iframe>
            <hr class="separator" />
            <div class="q-px-md button-map">
                <input type="button" class="btnsubmit" value="Go Line" />
            </div>
        </div>
    </div>
</template>

<script>
import { defineComponent } from "@vue/composition-api";

export default defineComponent({
    data() {
        return {
            center: { lat: 52.431944, lng: 10.803889 },
            markers: [{}, {}],
        };
    },
});
</script>

<style lang="scss" scoped>
.separator {
    width: 60px;
    height: 4px;
    border: none;
    background: var(--neutral-10);
    margin: 0 auto;
    border-radius: 8px;
    text-align: center;
    margin: 24px auto;
}

.button-map {
    text-align: center;
}
</style>
