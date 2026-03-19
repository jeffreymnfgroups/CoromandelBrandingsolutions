<template>
    <div>
        <div class="container">
            <div class="content">
                <div class="slider">
                    <div ref="reviewsRef" class="reviews">
                        <div v-for="review in reviews" ref="reviewRef" class="review">
                            <h1 v-html="review.title"></h1>
                            <p class="description">{{ review.description }}</p>
                            <p class="author">{{ review.author }}</p>
                            <p class="company">{{ review.company }}</p>
                        </div>
                    </div>
                    <div class="buttons">
                        <button :style="{ opacity: reviewIndex <= 0 ? .5 : 1 }" @click="prevReview"><img
                                src="@/assets/images/left-arrow.svg" alt=""></button>
                        <button :style="{ opacity: reviewIndex >= reviews.length - 1 ? .5 : 1 }" @click="nextReview"><img
                                src="@/assets/images/right-arrow.svg" alt=""></button>
                    </div>
                    <span class="quotes">
                        "
                    </span>
                </div>
            </div>
        </div>
    </div>
</template>


<script setup>
const reviewsRef = ref(null);
const reviewRef = ref(null);


const reviews = ref(
    [
        {
            title: 'Our Google reviews went from zero to over 200 in weeks',
            description: "I never realized how much our Google presence was holding us back. After working with this team, our profile was fully optimized, reviews started coming in consistently, and new customers kept mentioning they found us on Google. Best investment for our shop.",
            author: 'Ramesh Iyer',
            company: 'Iyer Textiles, Chennai'
        },
        {
            title: 'A website that actually brings in <br> new customers',
            description: "We had no online presence at all before this. They built us a clean, fast website and set up our Google Business Profile properly. Within the first month, we were getting calls directly from Google Search. The whole process was smooth and they explained everything clearly.",
            author: 'Priya Nair',
            company: 'Nair Catering Services, Coimbatore'
        },
        {
            title: '5-star reviews and more walk-ins every single week',
            description: "The GBP optimization they did for our clinic was a game changer. We went from barely showing up in local search to ranking in the top three. Our 5-star reviews doubled and new patients regularly tell us they chose us based on our Google rating. Highly recommend.",
            author: 'Dr. Karthik Selvam',
            company: 'Selvam Dental Clinic, Madurai'
        },
    ]
);


const reviewIndex = ref(0);


onMounted(() => {
    window.addEventListener("resize", handleWindowSizeChange);
    handleWindowSizeChange();
});
onUnmounted(() => {
    window.removeEventListener("resize", handleWindowSizeChange);
});


const handleWindowSizeChange = () => {
    reviewsRef.value.style.translate = `${reviewRef.value[0].offsetWidth * (reviewIndex.value * -1)}px 0`;
};


const nextReview = () => {
    if (reviewIndex.value >= reviews.value.length - 1) return;
    reviewIndex.value += 1;
    reviewsRef.value.style.translate = `${reviewRef.value[0].offsetWidth * (reviewIndex.value * -1)}px 0`;
    console.log(reviewIndex.value);
}


const prevReview = () => {
    if (reviewIndex.value <= 0) return;
    reviewIndex.value -= 1;
    reviewsRef.value.style.translate = `${reviewRef.value[0].offsetWidth * (reviewIndex.value * -1)}px 0`;
}


</script>


<style lang="scss" scoped>
div.container {
    & div.content {
        box-sizing: border-box;
        max-width: 1920px;
        margin: auto;
        padding: 0 100px;


        & div.slider {
            position: relative;
            box-sizing: border-box;
            max-width: 1100px;
            background: linear-gradient(96.65deg, #FF9A63 0%, #FE804B 100%);
            border: 10px solid #FFFFFF;
            border-radius: 40px;
            margin: auto;
            overflow: hidden;
            translate: 0 -110px;


            & div.reviews {
                display: flex;
                transition: translate .2s ease-in-out;


                & div.review {
                    box-sizing: border-box;
                    padding: 50px;
                    flex: 1 0 100%;


                    & h1 {
                        max-width: 70%;
                        margin-top: 0;
                        font-family: 'Archivo';
                        font-style: normal;
                        font-weight: 600;
                        font-size: 58px;
                        line-height: 68px;
                        letter-spacing: -1px;
                        color: #FFFFFF;


                        @media (max-width: 750px) {
                            max-width: 100%;
                            font-family: 'Archivo';
                            font-style: normal;
                            font-weight: 600;
                            font-size: 40px;
                            line-height: 50px;
                            letter-spacing: -0.75px;
                            color: #FFFFFF;
                            margin-top: 50px;
                        }
                    }


                    & p.description {
                        font-family: 'Archivo';
                        font-style: normal;
                        font-weight: 400;
                        font-size: 25px;
                        line-height: 38px;
                        letter-spacing: -0.5px;
                        color: #FFFFFF;
                        opacity: 0.8;


                        @media (max-width: 750px) {
                            font-weight: 400;
                            font-size: 22px;
                            line-height: 38px;
                            letter-spacing: -0.5px;
                        }
                    }


                    & p.author {
                        font-family: 'Inter';
                        font-style: normal;
                        font-weight: 600;
                        font-size: 20px;
                        line-height: 30px;
                        color: #FFFFFF;
                        margin-bottom: 0;
                    }


                    & p.company {
                        font-family: 'Inter';
                        font-style: normal;
                        font-weight: 400;
                        font-size: 16px;
                        line-height: 24px;
                        color: #FFFFFF;
                        opacity: 0.8;
                        margin-bottom: 0;
                        margin-top: 0;
                    }


                    @media (max-width: 700px) {
                        padding-bottom: 70px;
                        padding-left: 20px;
                        padding-right: 20px;
                    }
                }
            }


            & div.buttons {
                display: flex;
                align-items: center;
                justify-content: center;
                gap: 44px;
                position: absolute;
                bottom: 50px;
                right: 50px;


                & button {
                    all: unset;
                    padding: 10px 10px;


                    &:hover {
                        cursor: pointer;
                    }
                }


                @media (max-width: 700px) {
                    left: 0px;
                    right: 0px;
                    margin: auto;
                    bottom: 20px;
                }
            }


            & span.quotes {
                position: absolute;
                top: 50px;
                right: 50px;
                font-family: 'Archivo';
                font-style: normal;
                font-weight: 600;
                font-size: 200px;
                line-height: 0px;
                letter-spacing: -1px;
                color: #FFFFFF;
                transform: rotate(180deg);


                @media (max-width: 700px) {
                    font-size: 100px;
                }
            }
        }


        @media (max-width: 600px) {
            padding: 0 20px;
        }
    }
}
</style>
