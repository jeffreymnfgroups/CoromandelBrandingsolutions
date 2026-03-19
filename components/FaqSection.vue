<template>
    <div>
        <div class="container">
            <div class="content">
                <div class="left">
                    <h1>Frequently asked <br> questions</h1>
                    <img src="@/assets/images/stars.png" alt="">
                </div>

                <div class="right">
                    <ul>
                        <li v-for="item in accordion" @click="handleAccordionClick(item)">
                            <div class="title">{{ item.question }} <img :style="{ rotate: item.isOpen ? '180deg' : '0deg' }"
                                    src="@/assets/images/arrow.png" alt=""></div>
                            <p v-if="item.isOpen">{{ item.answer }}</p>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>


<script setup>
const accordion = ref([
    {
        question: "Do I really need a website for my business?",
        answer: "Yes. Most customers search online before visiting or calling a business. Without a website, you lose credibility and miss out on customers who simply can't find you. A website works for your business 24/7 even when you're closed.",
        isOpen: false
    },
    {
        question: "How do Google Reviews help my business?",
        answer: "Google Reviews are one of the strongest trust signals for new customers. Businesses with more 5-star reviews rank higher in local search results and get significantly more calls, walk-ins, and inquiries than competitors with fewer reviews.",
        isOpen: false
    },
    {
        question: "What is Google Business Profile optimization?",
        answer: "GBP optimization means setting up and fine-tuning your free Google Business listing so your business appears prominently in Google Search and Maps. It includes accurate details, photos, categories, and a strategy to consistently collect positive reviews.",
        isOpen: false
    },
    {
        question: "How long does it take to see results?",
        answer: "Most clients start seeing improvements in calls and visibility within the first 30 days of GBP optimization. Website results build steadily over 60 to 90 days as Google indexes your pages and your reviews grow.",
        isOpen: false
    },
    {
        question: "Will this work for my type of business?",
        answer: "Yes. We work with all kinds of local Indian businesses — restaurants, clinics, salons, retail shops, service providers and more. If customers search for what you offer on Google, we can help you get found first.",
        isOpen: false
    },
    {
        question: "What if I already have a website and Google listing?",
        answer: "We audit what you already have and identify exactly what's holding you back. Most existing websites and listings have clear gaps in speed, content, or reviews that are costing you customers. We fix those and build on what's already working.",
        isOpen: false
    }
])

const handleAccordionClick = (clickedQuestion) => {
    clickedQuestion.isOpen = !clickedQuestion.isOpen;

    accordion.value.forEach(question => {
        if (clickedQuestion !== question) {
            question.isOpen = false;
        }
    });
}
</script>


<style lang="scss" scoped>
div.container {
    & div.content {
        box-sizing: border-box;
        margin: auto;
        max-width: 1920px;
        padding: 0 100px;
        display: flex;
        gap: 20px;

        & div.left {
            width: 50%;
            display: flex;
            flex-direction: column;

            & h1 {
                margin-top: 0;
                font-family: 'Archivo';
                font-style: normal;
                font-weight: 600;
                font-size: 58px;
                line-height: 68px;
                letter-spacing: -1px;
                color: #FFFFFF;

                @media (max-width:600px) {
                    font-weight: 600;
                    font-size: 40px;
                    line-height: 50px;
                    letter-spacing: -0.75px;
                }
            }

            & img {
                max-width: 300px;
                margin-left: auto;
                margin-right: auto;
            }

            @media (max-width:850px) {
                width: 100%;
            }
        }

        & div.right {
            width: 50%;

            & ul {
                list-style: none;
                margin-left: 0;
                padding-left: 0;
                margin: 0;

                & li {
                    border-bottom: 1px solid rgba(255, 255, 255, 0.427);

                    & div.title {
                        align-items: center;
                        padding: 15px 0;
                        display: flex;
                        justify-content: space-between;
                        font-family: 'Archivo';
                        font-style: normal;
                        font-weight: 600;
                        font-size: 28px;
                        line-height: 38px;
                        letter-spacing: -0.5px;
                        color: #FFFFFF;

                        & img {
                            width: 24px;
                            height: 24px;
                        }
                    }

                    & p {
                        margin-top: 0px;
                        font-family: 'Inter';
                        font-style: normal;
                        font-weight: 400;
                        font-size: 16px;
                        line-height: 24px;
                        color: #FFFFFF;
                        opacity: 0.6;
                    }

                    &:last-of-type {
                        border: none;
                    }

                    &:hover {
                        cursor: pointer;
                    }
                }
            }

            @media (max-width:850px) {
                width: 100%;
            }
        }

        @media (max-width:850px) {
            flex-direction: column;
        }

        @media (max-width:600px) {
            padding: 0 20px;
        }
    }
}
</style>
