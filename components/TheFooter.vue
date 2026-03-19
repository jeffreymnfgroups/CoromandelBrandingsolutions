<template>
    <div>
        <div class="container">
            <div class="content">
                <div class="top">
                    <div class="logo">Coromandel Branding Solutions</div>
                    <div class="email-container">
                        <span>Send us an email at</span>
                        <button>hello@yourbrand.in</button>
                    </div>
                </div>
                <div class="bottom">
                    <div class="columns">
                        <div class="column">
                            <h2>About Us</h2>
                            <p>Chennai, Tamil Nadu, India</p>
                            <p>hello@yourbrand.in</p>
                            <p>+91 98765 43210</p>
                        </div>
                        <div class="column">
                            <h2>Quick Links</h2>
                            <NuxtLink to="/"><p>Home</p></NuxtLink>
                            <NuxtLink to="/#about"><p>About</p></NuxtLink>
                            <NuxtLink to="/#services"><p>Services</p></NuxtLink>
                            <NuxtLink to="/#results"><p>Results</p></NuxtLink>
                            <NuxtLink to="/contact"><p>Contact</p></NuxtLink>
                            <p>Blog</p>
                        </div>
                    </div>
                    <div class="columns">
                        <div class="column">
                            <h2>Our Services</h2>
                            <p>Website Design</p>
                            <p>Google Reviews</p>
                            <p>GBP Optimization</p>
                            <p>Local SEO</p>
                        </div>
                        <div class="column">
                            <h2>Industries</h2>
                            <p>Restaurants</p>
                            <p>Clinics</p>
                            <p>Retail Shops</p>
                            <p>Salons</p>
                            <p>Service Providers</p>
                        </div>
                        <div class="column">
                            <h2>We Serve</h2>
                            <p>Chennai</p>
                            <p>Bangalore</p>
                            <p>Coimbatore</p>
                            <p>Madurai</p>
                            <p>Pan India</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
</script>

<style lang="scss" scoped>
div.container {
    background: linear-gradient(151.98deg, #182E76 15.31%, #37233B 100%);
    padding-top: 100px;
    padding-bottom: 100px;
    border-radius: 100px 100px 0 0;
    width: 100vw;
    margin-top: 100px;

    & div.content {
        box-sizing: border-box;
        max-width: 1920px;
        margin: auto;
        padding: 0 100px;

        & div.top {
            display: flex;
            justify-content: space-between;
            align-items: center;
            border-bottom: 1px solid rgba(255, 255, 255, 0.427);
            padding-bottom: 40px;

            & div.logo {
                font-family: 'Archivo';
                font-weight: 800;
                font-size: 22px;
                color: #FFFFFF;
                letter-spacing: -0.5px;
                white-space: nowrap;
            }

            & div.email-container {
                display: flex;
                align-items: center;
                gap: 20px;

                & span {
                    font-family: 'Inter';
                    font-style: normal;
                    font-weight: 400;
                    font-size: 16px;
                    line-height: 24px;
                    text-align: right;
                    color: #FFFFFF;
                }

                & button {
                    all: unset;
                    display: block;
                    width: 220px;
                    height: 56px;
                    font-family: 'Inter';
                    font-style: normal;
                    font-weight: 500;
                    font-size: 16px;
                    line-height: 24px;
                    text-align: center;
                    color: #FFFFFF;
                    background-color: #FE804B;
                    border-radius: 12px;
                    transition: background-color .2s ease-in-out;

                    &:hover {
                        background-color: #FF9A63;
                        cursor: pointer;
                    }

                    @media only screen and (max-width: 450px) {
                        width: 100%;
                    }
                }

                @media only screen and (max-width: 600px) {
                    flex-direction: column;
                    align-items: flex-start;
                    width: 100%;
                }
            }

            @media only screen and (max-width: 600px) {
                flex-direction: column;
                align-items: flex-start;
                gap: 10px;
            }
        }

        & div.bottom {
            padding-top: 20px;
            display: flex;
            justify-content: space-between;
            gap: 60px;
            flex-wrap: wrap;

            & div.columns {
                display: flex;
                gap: 60px;
                flex-wrap: wrap;

                & h2 {
                    font-family: 'Inter';
                    font-style: normal;
                    font-weight: 600;
                    font-size: 20px;
                    line-height: 30px;
                    color: #FFFFFF;
                    margin-bottom: 20px;
                }

                & a {
                    text-decoration: none;
                }

                & p {
                    font-family: 'Inter';
                    font-style: normal;
                    font-weight: 400;
                    font-size: 16px;
                    line-height: 24px;
                    color: #FFFFFF;
                    opacity: 0.6;
                    margin: 8px 0;
                    transition: opacity .2s ease-in-out;

                    &:hover {
                        opacity: 1;
                        cursor: pointer;
                    }
                }

                @media only screen and (max-width: 1200px) {
                    gap: 20px;
                    justify-content: space-between;
                }
            }

            @media only screen and (max-width: 1200px) {
                gap: 20px;
            }
        }

        @media only screen and (max-width: 600px) {
            padding: 0 20px;
        }
    }

    @media only screen and (max-width: 600px) {
        padding-top: 50px;
    }
}
</style>
