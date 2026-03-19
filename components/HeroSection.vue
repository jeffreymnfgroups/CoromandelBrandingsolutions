<template>
    <div>
        <div class="hero-container">
            <div class="content">
                <h1 class="heading">We develop the <img class="mail" src="@/assets/images/mail.png" alt=""> eye <br> <img
                        src="@/assets/images/arrows.svg" alt=""> catching brands
                </h1>
               <p class="subheading">Get found on Google, build trust with reviews <br>
                and grow your business with a website <br>
                that works for you.
            </p>

                <NuxtLink to="/contact"><button class="contact-cta">Contact Us</button></NuxtLink>
            </div>
            <img class="wave" src="@/assets/images/wave2.svg" alt="">
        </div>
    </div>
</template>


<script setup>
</script>


<style lang="scss" scoped>
div.hero-container {
    padding-top: 200px;
    padding-bottom: 60px;
    position: relative;

    & div.content {
        max-width: 1920px;
        margin: auto;
        padding: 0 100px;
        z-index: 1;
        box-sizing: border-box;

        & h1.heading {
            max-width: 80%;
            margin: 0px;
            font-family: 'Archivo';
            font-style: normal;
            font-weight: 800;
            font-size: 98px;
            line-height: 108px;
            letter-spacing: -3px;
            color: #183282;

            & img {
                &.mail {
                    width: 90px;
                }
            }

            @media only screen and (max-width: 1460px) {
                & br {
                    display: none;
                }
            }

            @media only screen and (max-width: 1100px) {
                max-width: 70%;
                font-size: 68px;
                line-height: 100%;

                & img {
                    width: 68px !important;

                    &.mail {
                        translate: 0 10px;
                    }
                }
            }

            @media only screen and (max-width: 700px) {
                font-size: 48px;
                line-height: 140%;
                max-width: 90%;

                & img {
                    width: 48px !important;

                    &.mail {
                        translate: 0 5px;
                    }
                }
            }

            @media only screen and (max-width: 450px) {
                font-size: 36px;
                line-height: 130%;
                max-width: 100%;
                letter-spacing: -1.5px;

                & img {
                    width: 34px !important;

                    &.mail {
                        translate: 0 4px;
                    }
                }
            }

            @media only screen and (max-width: 360px) {
                font-size: 30px;
                letter-spacing: -1px;

                & img {
                    width: 28px !important;
                }
            }
        }

        & p.subheading {
            font-family: 'Inter';
            font-style: normal;
            font-weight: 400;
            font-size: 20px;
            line-height: 30px;
            color: #183282;
            opacity: 0.8;
            margin-top: 30px;
            margin-bottom: 60px;

            @media only screen and (max-width: 700px) {
                & br {
                    display: none;
                }
            }

            @media only screen and (max-width: 450px) {
                font-size: 16px;
                line-height: 26px;
                margin-top: 20px;
                margin-bottom: 40px;
            }
        }

        & button.contact-cta {
            all: unset;
            width: 164px;
            height: 56px;
            text-align: center;
            font-family: 'Inter';
            font-style: normal;
            font-weight: 500;
            font-size: 16px;
            line-height: 24px;
            color: #FFFFFF;
            background-color: #FE804B;
            border-radius: 12px;
            transition: background-color .2s ease-in-out;

            &:hover {
                background-color: #FF9A63;
                cursor: pointer;
            }

            &:active {
                background-color: #FE804B;
            }

            @media only screen and (max-width: 450px) {
                width: 100%;
                height: 52px;
            }
        }

        @media only screen and (max-width: 1100px) {
            padding: 0 40px;
            padding-bottom: 180px;
        }

        @media only screen and (max-width: 700px) {
            padding: 0 24px;
            padding-bottom: 200px;
        }

        @media only screen and (max-width: 450px) {
            padding: 0 20px;
            padding-bottom: 160px;
        }
    }

    & img.wave {
        position: absolute;
        top: 220px;
        right: 100px;
        z-index: -1;

        @media only screen and (max-width: 1100px) {
            scale: .8;
            right: 0px;
        }

        @media only screen and (max-width: 700px) {
            scale: .6;
            bottom: 0px;
            top: auto;
            right: -80px;
        }

        @media only screen and (max-width: 450px) {
            scale: .45;
            right: -120px;
            bottom: -20px;
        }

        @media only screen and (max-width: 360px) {
            scale: .35;
            right: -140px;
            bottom: -40px;
        }
    }

    @media only screen and (max-width: 700px) {
        padding-top: 120px;
        padding-bottom: 40px;
    }

    @media only screen and (max-width: 450px) {
        padding-top: 100px;
        padding-bottom: 20px;
    }
}
</style>
