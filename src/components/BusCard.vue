<template>
    <div class="cardbus">
        <div class="container">
            <div class="header-cardbus">
                <div id="style" :style="style" class="color">
                    <p class="line-number">{{ Numero }}</p>
                </div>
            </div>

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
            return "background: " + this.Color + ";";
        },

        hoverstyle: function () {
            return "--borderHover: 1px solid " + this.Color;
        },
    },

    setup() {
        return {};
    },
});
</script>

<style lang="scss" scoped>
.cardbus {
    width: calc(100% / 5 - 20px);
    height: 192px;
    background: var(--white);
    box-shadow: var(--shadow-soft), inset 0 0 0 1px var(--white);
    border-radius: 24px;
    display: inline-block;
    margin: 24px 24px 0 0;
    transition: var(--transition);
    cursor: pointer;

    &:hover {
        box-sizing: border-box;
        box-shadow: var(--shadow-soft), inset 0 0 0 1px var(--neutral-80);
        border-radius: 24p;
    }

    &:nth-child(5n) {
        margin-right: 0;
    }

    /* START custom line colors */
    &.line-201 {
        &:hover {
            box-shadow: 0px 8px 16px 0px rgba(var(--c201-rgb), 0.35), inset 0 0 0 1px var(--c201);
        }
    }

    &.line-202 {
        &:hover {
            box-shadow: 0px 8px 16px 0px rgba(var(--c202-rgb), 0.35), inset 0 0 0 1px var(--c202);
        }
    }

    &.line-203 {
        &:hover {
            box-shadow: 0px 8px 16px 0px rgba(var(--c203-rgb), 0.35), inset 0 0 0 1px var(--c203);
        }
    }

    &.line-204 {
        &:hover {
            box-shadow: 0px 8px 16px 0px rgba(var(--c204-rgb), 0.35), inset 0 0 0 1px var(--c204);
        }
    }

    &.line-211 {
        &:hover {
            box-shadow: 0px 8px 16px 0px rgba(var(--c211-rgb), 0.35), inset 0 0 0 1px var(--c211);
        }
    }

    &.line-212 {
        &:hover {
            box-shadow: 0px 8px 16px 0px rgba(var(--c212-rgb), 0.35), inset 0 0 0 1px var(--c212);
        }
    }

    &.line-213 {
        &:hover {
            box-shadow: 0px 8px 16px 0px rgba(var(--c213-rgb), 0.35), inset 0 0 0 1px var(--c213);
        }
    }

    &.line-215 {
        &:hover {
            box-shadow: 0px 8px 16px 0px rgba(var(--c215-rgb), 0.35), inset 0 0 0 1px var(--c215);
        }
    }

    &.line-216 {
        &:hover {
            box-shadow: 0px 8px 16px 0px rgba(var(--c216-rgb), 0.35), inset 0 0 0 1px var(--c216);
        }
    }

    &.line-218 {
        &:hover {
            box-shadow: 0px 8px 16px 0px rgba(var(--c218-rgb), 0.35), inset 0 0 0 1px var(--c218);
        }
    }
    /* FIN custom line colors */

    .container {
        padding: 16px;
        display: flex;
        flex-wrap: wrap;

        .header-cardbus {
            width: 100%;
            line-height: 100%;

            &::after {
                content: "";
                display: inline-block;
                background-color: var(--neutral-10);
                height: 4px;
                width: 70px;
                border-radius: 4px;
                margin: 16px calc(50% - 35px);
            }

            .color {
                text-align: center;
                justify-content: center;
                align-items: center;
                width: auto;
                height: 60px;
                border-radius: 16px;
                display: flex;

                .line-number {
                    font-family: Source Sans Pro;
                    font-style: normal;
                    font-weight: normal;
                    font-size: 16px;
                    line-height: 140%;
                    font-weight: 600;
                    color: var(--white);
                }
            }
        }

        .separator {
            display: inline-block;
            width: 70px;
            height: 4px;
            border: none;
            background: var(--neutral-10);
            border-radius: 8px;
            text-align: center;
            margin: 16px auto;
        }

        .text {
            p {
                font-weight: 400;
                margin-bottom: 8px;
            }
        }
    }
}

/* ----------------------------------- 1200px */
@media (max-width: 1200px) {
    .cardbus {
        width: calc(100% / 4 - 20px);

        &:nth-child(4n) {
            margin-right: 0;
        }

        &:nth-child(5n) {
            margin-right: 24px;
        }
    }
}

/* ----------------------------------- 680px */
@media (max-width: 680px) {
    .cardbus {
        width: calc(100% / 2 - 8px);
        margin: 16px 16px 0 0;

        &:nth-child(4n) {
            margin-right: 16px;
        }

        &:nth-child(5n) {
            margin-right: 16px;
        }

        &:nth-child(2n) {
            margin-right: 0;
        }
    }
}
</style>
