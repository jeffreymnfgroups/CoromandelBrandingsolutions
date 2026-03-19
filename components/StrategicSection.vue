<template>
  <div>
    <div class="container">
      <div class="content">
        <h2>Helping Indian businesses <br> grow online</h2>
        <div ref="cards" class="cards">
          <div class="card">
            <span class="value">{{ counters.businesses.count }}+</span>
            <span class="info">Indian businesses empowered with a digital presence</span>
          </div>
          <div class="card">
            <span class="value">{{ counters.reviews.count }}k+</span>
            <span class="info">Google Reviews generated for our clients</span>
          </div>
          <div class="card">
            <span class="value">{{ counters.cities.count }}+</span>
            <span class="info">Cities across India served and growing</span>
          </div>
          <div class="card">
            <span class="value">{{ counters.rating.count }}★</span>
            <span class="info">Average Google rating achieved for clients</span>
          </div>
        </div>
        <button>Contact Us</button>
      </div>

      <!-- SVG replacing coin.png -->
      <svg class="coin-svg" viewBox="0 0 200 340" fill="none" xmlns="http://www.w3.org/2000/svg">
        <!-- Outer ring -->
        <circle cx="100" cy="170" r="90" stroke="rgba(254,128,75,0.18)" stroke-width="1.5"/>
        <circle cx="100" cy="170" r="70" stroke="rgba(254,128,75,0.12)" stroke-width="1"/>
        <!-- Coin body -->
        <circle cx="100" cy="170" r="58" fill="url(#coinGrad)" />
        <!-- Inner ring detail -->
        <circle cx="100" cy="170" r="48" stroke="rgba(255,255,255,0.12)" stroke-width="1"/>
        <!-- Rupee symbol -->
        <text x="100" y="187" text-anchor="middle"
          font-family="Arial" font-size="48" font-weight="700"
          fill="rgba(255,255,255,0.9)">₹</text>
        <!-- Orbit dot top -->
        <circle cx="100" cy="80" r="5" fill="#FE804B" opacity="0.7"/>
        <!-- Orbit dot right -->
        <circle cx="190" cy="170" r="4" fill="#FE804B" opacity="0.4"/>
        <!-- Orbit dot left -->
        <circle cx="10" cy="170" r="3" fill="rgba(254,128,75,0.3)"/>
        <!-- Sparkle top-right -->
        <path d="M158 60 L161 68 L169 71 L161 74 L158 82 L155 74 L147 71 L155 68 Z"
          fill="rgba(254,128,75,0.5)"/>
        <!-- Sparkle bottom-left -->
        <path d="M38 260 L40 266 L46 268 L40 270 L38 276 L36 270 L30 268 L36 266 Z"
          fill="rgba(255,255,255,0.2)"/>
        <defs>
          <radialGradient id="coinGrad" cx="40%" cy="35%" r="65%">
            <stop offset="0%" stop-color="#FE9A63"/>
            <stop offset="100%" stop-color="#c75b28"/>
          </radialGradient>
        </defs>
      </svg>

    </div>
  </div>
</template>

<script setup>
const counters = ref({
  businesses: {
    count: 1,
    maxCount: 500
  },
  reviews: {
    count: 1,
    maxCount: 10
  },
  cities: {
    count: 1,
    maxCount: 25
  },
  rating: {
    count: 1,
    maxCount: 5
  },
})

const cards = ref(null)

const countUp = (counters, timeToExecute) => {
  for (const counter in counters) {
    const intervalId = setInterval(() => {
      counters[counter].count++
      if (counters[counter].count == counters[counter].maxCount) clearInterval(intervalId)
    }, timeToExecute / counters[counter].maxCount)
  }
}

onMounted(() => {
  const observer = new IntersectionObserver((entries) => {
    entries.forEach((entry) => {
      if (entry.intersectionRatio > 0) {
        setTimeout(() => {
          countUp(counters.value, 1700)
        }, 100)
        observer.disconnect()
      }
    })
  })
  observer.observe(cards.value)
})
</script>

<style lang="scss" scoped>
div.container {
  padding-top: 80px;
  position: relative;

  & div.content {
    box-sizing: border-box;
    max-width: 1920px;
    padding: 0 100px;
    margin: auto;

    & h2 {
      position: relative;
      z-index: 2;
      font-family: 'Archivo';
      font-style: normal;
      font-weight: 600;
      font-size: 58px;
      line-height: 68px;
      text-align: center;
      letter-spacing: -1px;
      color: #FFFFFF;
      margin-bottom: 100px;

      @media (max-width: 780px) {
        font-size: 40px;
        line-height: 50px;
        text-align: center;
        letter-spacing: -0.75px;
        margin-bottom: 50px;

        & br {
          display: none;
        }
      }
    }

    & div.cards {
      display: flex;
      justify-content: center;
      gap: 36px;
      flex-wrap: wrap;
      margin: auto;
      margin-bottom: 50px;

      @media (max-width: 1395px) {
        max-width: calc(273px * 2 + 36px);
      }

      & div.card {
        width: 272px;
        background-color: #FFFFFF;
        border-radius: 12px;
        display: flex;
        flex-direction: column;
        box-sizing: border-box;
        justify-content: center;
        padding: 30px;
        z-index: 2;

        & span.value {
          font-family: 'Archivo';
          font-style: normal;
          font-weight: 800;
          font-size: 78px;
          line-height: 88px;
          letter-spacing: -3px;
          color: #183282;
        }

        & span.info {
          font-family: 'Inter';
          font-style: normal;
          font-weight: 400;
          font-size: 16px;
          line-height: 24px;
          color: #183282;
          opacity: 0.8;
        }

        @media (max-width: 450px) {
          width: 90%;
        }
      }

      z-index: 2;
    }

    & button {
      all: unset;
      display: block;
      margin: 0 auto;
      width: 164px;
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
      margin-bottom: 80px;
      cursor: pointer;

      &:hover {
        background-color: #FF9A63;
      }

      @media only screen and (max-width: 450px) {
        width: 100%;
      }
    }

    @media (max-width: 780px) {
      padding: 0 20px;
    }
  }

  & svg.coin-svg {
    position: absolute;
    right: -10px;
    top: 0px;
    width: 188px;
    z-index: 1;

    @media (max-width: 800px) {
      display: none;
    }
  }

  @media (max-width: 780px) {
    padding-top: 0;
  }
}
</style>
