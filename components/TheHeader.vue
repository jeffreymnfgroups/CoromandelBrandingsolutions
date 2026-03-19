<template>
    <div class="the-header-root">
        <div :class="{'mobile-menu': true, 'open': mobileMenuOpen}">
            <div class="nav-list">
                <NuxtLink to="/" :class="{'nav-item': true, 'open': mobileMenuOpen}" @click="mobileMenuOpen = false">Home</NuxtLink>
                <NuxtLink to="/#services" :class="{'nav-item': true, 'open': mobileMenuOpen}" @click="mobileMenuOpen = false">Services</NuxtLink>
                <NuxtLink to="/#results" :class="{'nav-item': true, 'open': mobileMenuOpen}" @click="mobileMenuOpen = false">Results</NuxtLink>
                <NuxtLink to="/#about" :class="{'nav-item': true, 'open': mobileMenuOpen}" @click="mobileMenuOpen = false">About Us</NuxtLink>
                <NuxtLink to="/contact" :class="{'nav-item': true, 'open': mobileMenuOpen}" @click="mobileMenuOpen = false">Contact</NuxtLink>
            </div>
        </div>
        <div>
            <div class="header-container">
                <div class="header">
                    <NuxtLink to="/" class="logo">Coromandel Branding Solutions</NuxtLink>
                    <div class="nav-container">
                        <NuxtLink to="/" class="nav-item">Home</NuxtLink>
                        <NuxtLink to="/#services" class="nav-item">Services</NuxtLink>
                        <NuxtLink to="/#results" class="nav-item">Results</NuxtLink>
                        <NuxtLink to="/#about" class="nav-item">About Us</NuxtLink>
                        <NuxtLink to="/contact" class="nav-item">Contact</NuxtLink>
                    </div>
                    <NuxtLink to="/contact" class="contact-cta">Contact Us</NuxtLink>
                </div>
            </div>
            <div class="mobile-container">
                <div class="header">
                    <NuxtLink to="/" class="logo">Coromandel Branding Solutions</NuxtLink>
                    <div @click="mobileMenuOpen = !mobileMenuOpen" :class="{'menu-button': true}">
                        <div v-if="!mobileMenuOpen" class="open">
                            <div class="bar"></div>
                            <div class="bar"></div>
                            <div class="bar"></div>
                        </div>
                        <div v-else class="close">
                            <div class="bar"></div>
                            <div class="bar"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue'
const mobileMenuOpen = ref(false);
</script>

<style lang="scss" scoped>
div.header-container {
    box-sizing: border-box;
    position: fixed;
    top: 0px;
    height: 100px;
    width: 100vw;
    background-color: #ECEADD;
    filter: blur(0);
    z-index: 99;

    & div.header {
        box-sizing: border-box;
        padding: 0 100px;
        height: 100%;
        max-width: 1920px;
        margin: auto;
        display: flex;
        justify-content: space-between;
        align-items: center;

        .logo {
            font-family: 'Archivo';
            font-weight: 800;
            font-size: 20px;
            color: #183282;
            letter-spacing: -0.5px;
            white-space: nowrap;
            text-decoration: none;
        }

        & .nav-container {
            display: flex;
            gap: 32px;

            & .nav-item {
                font-family: 'Inter';
                font-style: normal;
                font-weight: 400;
                font-size: 16px;
                line-height: 24px;
                color: #183282;
                opacity: 0.8;
                transition: .2s ease-in-out opacity;
                text-decoration: none;

                &:hover {
                    opacity: 1;
                    cursor: pointer;
                }
            }
        }

        & .contact-cta {
            display: inline-block;
            width: 144px;
            height: 48px;
            line-height: 48px;
            border: 1px solid #FE804B;
            border-radius: 12px;
            text-align: center;
            font-family: 'Inter';
            font-style: normal;
            font-weight: 500;
            font-size: 16px;
            color: #183282;
            transition: background-color .2s ease-in-out, color .2s ease-in-out;
            text-decoration: none;

            &:hover {
                cursor: pointer;
                background-color: #FE804B;
                color: white;
            }
        }
    }

    @media only screen and (max-width: 1100px) {
        display: none;
    }
}

div.mobile-container {
    display: none;
    z-index: 99;

    @media only screen and (max-width: 1100px) {
        display: block;

        box-sizing: border-box;
        padding: 0 20px;
        position: fixed;
        top: 0px;
        height: 80px;
        width: 100vw;
        background-color: #ECEADD;
        filter: blur(0);

        & div.header {
            position: relative;
            height: 100%;
            margin: auto;
            display: flex;
            justify-content: space-between;
            align-items: center;

            & .logo {
                font-family: 'Archivo';
                font-weight: 800;
                font-size: 15px;
                color: #183282;
                letter-spacing: -0.5px;
                white-space: nowrap;
                text-decoration: none;
            }

            & div.menu-button {
                position: absolute;
                right: 0px;
                width: 30px;
                height: 30px;

                & div.bar {
                    background-color: rgb(132, 132, 132);
                    opacity: 1;
                    height: 4px;
                    width: 30px;
                    border-radius: 100px;
                    transition: background-color .2s ease-in-out;
                }

                & div.open {
                    display: flex;
                    flex-direction: column;
                    gap: 5px;
                }

                & div.close {
                    position: absolute;

                    & div.bar {
                        position: absolute;
                        top: 13px;
                        left: 0;

                        &:first-of-type {
                            rotate: -45deg;
                        }

                        &:last-of-type {
                            rotate: 45deg;
                        }
                    }
                }

                &:hover {
                    & div.bar {
                        background-color: black;
                    }

                    cursor: pointer;
                }
            }
        }
    }
}

div.mobile-menu {
    translate: -100% 0;

    @media only screen and (min-width: 1100px) {
        display: none;
    }

    position: fixed;
    z-index: 99;
    min-height: 100vh;
    width: 100vw;
    background-color: #ECEADD;
    display: flex;
    justify-content: center;
    align-items: center;
    filter: blur(0);

    & div.nav-list {
        display: flex;
        flex-direction: column;
        gap: 30px;

        & .nav-item {
            font-family: 'Archivo';
            font-style: normal;
            font-weight: 800;
            font-size: 48px;
            line-height: 58px;
            letter-spacing: -2px;
            color: #183282;
            text-decoration: none;

            &:hover {
                cursor: pointer;
            }

            translate: -400px 0;
            opacity: 0;

            &:first-of-type {
                transition: translate .2s ease-in-out, opacity .2s ease-in-out;
            }
            &:nth-of-type(2) {
                transition: translate .3s ease-in-out, opacity .2s ease-in-out;
            }
            &:nth-of-type(3) {
                transition: translate .4s ease-in-out, opacity .4s ease-in-out;
            }
            &:nth-of-type(4) {
                transition: translate .5s ease-in-out, opacity .5s ease-in-out;
            }
            &:last-of-type {
                transition: translate .6s ease-in-out, opacity .6s ease-in-out;
            }

            &.open {
                translate: 0px 0;
                opacity: 1;
            }
        }
    }

    transition: translate .2s ease-in-out;

    &.open {
        translate: 0 0;
    }
}
</style>
