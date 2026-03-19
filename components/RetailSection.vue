<template>
    <div>
        <div class="container" id="results">
            <img class="bg" src="@/assets/images/background.png" alt="">

            <div class="content">
                <img class="star" src="@/assets/images/Star.png" alt="">
                <h2>Retail franchise digital <br> marketing</h2>

                <div class="cards">

                    <!-- Plan 1 -->
                    <div class="card">
                        <div class="card-header">
                            <h3>Starter Visibility Pack</h3>
                            <p>For businesses just getting started online</p>
                        </div>
                        <div class="features">
                            <div class="feature">
                                <span class="check">✓</span>
                                <span class="feature-name">Google Business Profile (GBP) setup & optimization</span>
                            </div>
                            <div class="feature">
                                <span class="check">✓</span>
                                <span class="feature-name">QR code for store location & directions</span>
                            </div>
                            <div class="feature">
                                <span class="check">✓</span>
                                <span class="feature-name">QR code to collect customer reviews</span>
                            </div>
                        </div>
                        <div class="pricing-block">
                            <div class="original-price">Total value: <s>₹6,000</s></div>
                            <div class="final-price">₹2,999</div>
                            <div class="saving-tag">You save ₹3,001</div>
                        </div>
                    </div>

                    <!-- Plan 2 - Featured -->
                    <div class="card featured">
                        <div class="popular-label">⭐ Most Popular</div>
                        <div class="card-header">
                            <h3>Local Growth Pack</h3>
                            <p>Maintain and grow your Google presence</p>
                        </div>
                        <div class="features">
                            <div class="feature">
                                <span class="check">✓</span>
                                <span class="feature-name">Everything in Starter Visibility Pack</span>
                            </div>
                            <div class="feature">
                                <span class="check">✓</span>
                                <span class="feature-name">GBP post guidance & strategy</span>
                            </div>
                            <div class="feature">
                                <span class="check">✓</span>
                                <span class="feature-name">Ready-to-use post & update templates</span>
                            </div>
                        </div>
                        <div class="pricing-block">
                            <div class="original-price">Total value: <s>₹8,000</s></div>
                            <div class="final-price">₹3,999</div>
                            <div class="saving-tag">You save ₹4,001 — 50% OFF</div>
                        </div>
                    </div>

                    <!-- Plan 3 -->
                    <div class="card">
                        <div class="limited-label">🔥 Limited Time Offer</div>
                        <div class="card-header">
                            <h3>Complete Business Pack</h3>
                            <p>Everything you need to generate leads online</p>
                        </div>
                        <div class="features">
                            <div class="feature">
                                <span class="check">✓</span>
                                <span class="feature-name">Everything in Local Growth Pack</span>
                            </div>
                            <div class="feature">
                                <span class="check">✓</span>
                                <span class="feature-name">Professional website with lead capture form</span>
                            </div>
                            <div class="feature">
                                <span class="check">✓</span>
                                <span class="feature-name">Domain setup & hosting configuration</span>
                            </div>
                        </div>
                        <div class="pricing-block">
                            <div class="original-price">Total value: <s>₹22,000</s></div>
                            <div class="final-price">₹5,999</div>
                            <div class="saving-tag">You save ₹16,001 — 73% OFF</div>
                        </div>
                    </div>

                </div>
                <NuxtLink to="/contact"><button>Contact Us</button></NuxtLink>
            </div>
        </div>
    </div>
</template>

<script setup></script>

<style lang="scss" scoped>
div.container {
    padding-top: 150px;
    position: relative;

    & div.content {
        position: relative;
        box-sizing: border-box;
        max-width: 1920px;
        padding: 0 100px;
        margin: auto;

        & h2 {
            font-family: 'Archivo';
            font-weight: 600;
            font-size: 58px;
            line-height: 68px;
            text-align: center;
            letter-spacing: -1px;
            color: #FFFFFF;
            margin-bottom: 100px;
            position: relative;
            z-index: 1;

            @media only screen and (max-width: 500px) {
                font-size: 40px;
                line-height: 50px;
                letter-spacing: -0.75px;
                margin-bottom: 50px;
                & br { display: none; }
            }
        }

        & div.cards {
            display: flex;
            justify-content: center;
            align-items: stretch; /* ← all cards same height */
            gap: 36px;
            margin-bottom: 50px;

            & div.card {
                width: 374px;
                background: #183282;
                border: 2px solid rgba(255, 255, 255, 0.2);
                border-radius: 20px;
                padding: 32px;
                display: flex;
                flex-direction: column;
                box-sizing: border-box;
                position: relative;

                /* Featured / Most Popular card */
                &.featured {
                    background: linear-gradient(180deg, #7796FD 0%, #4958CC 100%);
                    border: 2px solid #FFFFFF;
                    transform: scale(1.04);

                    @media only screen and (max-width: 1100px) {
                        transform: scale(1);
                    }
                }

                /* Labels */
                & .popular-label,
                & .limited-label {
                    font-family: 'Inter';
                    font-size: 13px;
                    font-weight: 600;
                    color: #fff;
                    background: rgba(255,255,255,0.15);
                    border-radius: 20px;
                    padding: 4px 12px;
                    display: inline-block;
                    margin-bottom: 12px;
                    letter-spacing: 0.3px;
                }

                & .card-header {
                    margin-bottom: 16px;

                    & h3 {
                        margin: 0 0 6px 0;
                        font-family: 'Archivo';
                        font-weight: 600;
                        font-size: 22px;
                        line-height: 30px;
                        letter-spacing: -0.5px;
                        color: #FFFFFF;
                    }

                    & p {
                        margin: 0;
                        font-family: 'Inter';
                        font-weight: 400;
                        font-size: 14px;
                        line-height: 22px;
                        color: rgba(255, 255, 255, 0.75);
                    }
                }

                & div.features {
                    flex: 1; /* pushes pricing-block to bottom */
                    margin-bottom: 20px;

                    & div.feature {
                        display: flex;
                        align-items: flex-start;
                        gap: 10px;
                        padding: 10px 0;
                        border-bottom: 1px solid rgba(255, 255, 255, 0.15);

                        &:last-of-type {
                            border-bottom: none;
                        }

                        & span.check {
                            font-size: 14px;
                            color: #A8F0C6;
                            flex-shrink: 0;
                            margin-top: 2px;
                        }

                        & span.feature-name {
                            font-family: 'Inter';
                            font-weight: 500;
                            font-size: 15px;
                            line-height: 22px;
                            color: #FFFFFF;
                        }
                    }
                }

                /* Pricing block — sits at the bottom of every card */
                & .pricing-block {
                    border-top: 1px solid rgba(255, 255, 255, 0.2);
                    padding-top: 16px;

                    & .original-price {
                        font-family: 'Inter';
                        font-size: 13px;
                        color: rgba(255,255,255,0.6);
                        margin-bottom: 6px;

                        & s { opacity: 0.7; }
                    }

                    & .final-price {
                        font-family: 'Archivo';
                        font-weight: 700;
                        font-size: 32px;
                        color: #FFFFFF;
                        letter-spacing: -1px;
                        line-height: 1;
                        margin-bottom: 6px;
                    }

                    & .saving-tag {
                        font-family: 'Inter';
                        font-size: 13px;
                        font-weight: 600;
                        color: #A8F0C6;
                        letter-spacing: 0.2px;
                    }
                }
            }

            @media only screen and (max-width: 1100px) {
                flex-wrap: wrap;
                align-items: flex-start;
            }
        }

        & button {
            all: unset;
            display: block;
            margin: 0 auto;
            width: 164px;
            height: 56px;
            font-family: 'Inter';
            font-weight: 500;
            font-size: 16px;
            line-height: 24px;
            text-align: center;
            color: #FFFFFF;
            background-color: #FE804B;
            border-radius: 12px;
            transition: background-color .2s ease-in-out;
            margin-bottom: 80px;
            cursor: pointer;

            &:hover {
                background-color: #FF9A63;
            }

            @media only screen and (max-width: 450px) {
                width: 100%;
            }
        }

        & img.star {
            position: absolute;
            top: 0;
            right: 0;
            width: 200px;
            padding-right: inherit;
            z-index: 0;

            @media screen and (max-width: 1100px) {
                display: none;
            }
        }

        @media only screen and (max-width: 700px) {
            padding: 0 20px;
        }
    }

    @media only screen and (max-width: 700px) {
        padding-top: 60px;
    }

    & img.bg {
        position: absolute;
        left: 0px;
        top: 50%;
    }
}
</style>
