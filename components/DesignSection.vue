<template>
  <div>
    <div class="container" id="services">
      <div class="content">
        <div class="info">

          <div class="eyebrow">
            <svg width="18" height="18" viewBox="0 0 24 24" fill="none">
              <path d="M12 22C17.5228 22 22 17.5228 22 12C22 6.47715 17.5228 2 12 2C6.47715 2 2 6.47715 2 12C2 17.5228 6.47715 22 12 22Z"
                stroke="#FE804B" stroke-width="1.5"/>
              <path d="M8 12h8M12 8v8" stroke="#FE804B" stroke-width="1.5" stroke-linecap="round"/>
            </svg>
            <span>Education — Why It Matters</span>
          </div>

          <h2>Be found.<br>Be trusted.<br>Be chosen.</h2>

          <p class="subtitle">
            Your website, reviews, and Google presence work
            together — or against you. Here's what actually moves the needle.
          </p>

          <div class="feature-list">
            <div class="feature-row">
              <div class="feature-left">
                <svg width="20" height="20" viewBox="0 0 24 24" fill="none">
                  <circle cx="12" cy="12" r="9" stroke="white" stroke-width="1.5"/>
                  <ellipse cx="12" cy="12" rx="3.5" ry="9" stroke="white" stroke-width="1.5"/>
                  <path d="M3 12h18" stroke="white" stroke-width="1.5" stroke-linecap="round"/>
                  <path d="M5 7.5h14M5 16.5h14" stroke="rgba(255,255,255,0.5)" stroke-width="1.2" stroke-linecap="round"/>
                </svg>
                <span class="label">Website</span>
              </div>
              <p class="feature-desc">Be found online and build instant credibility with every visitor.</p>
            </div>

            <div class="divider"></div>

            <div class="feature-row">
              <div class="feature-left">
                <svg width="20" height="20" viewBox="0 0 24 24" fill="none">
                  <path d="M12 2l2.4 7.4H22l-6.2 4.5 2.4 7.4L12 17l-6.2 4.3 2.4-7.4L2 9.4h7.6z"
                    stroke="white" stroke-width="1.5" stroke-linejoin="round" fill="none"/>
                </svg>
                <span class="label">Google Reviews</span>
              </div>
              <p class="feature-desc">Drive trust signals that attract new customers and rank you higher.</p>
            </div>

            <div class="divider"></div>

            <div class="feature-row">
              <div class="feature-left">
                <svg width="20" height="20" viewBox="0 0 24 24" fill="none">
                  <path d="M12 20V8" stroke="white" stroke-width="1.5" stroke-linecap="round"/>
                  <path d="M12 8c0 0 1.5-4 4-5-0.5 2-0.5 4 0 5" stroke="white" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                  <path d="M12 8c0 0-1.5-4-4-5 0.5 2 0.5 4 0 5" stroke="rgba(255,255,255,0.6)" stroke-width="1.4" stroke-linecap="round" stroke-linejoin="round"/>
                  <path d="M8 20h8" stroke="white" stroke-width="1.5" stroke-linecap="round"/>
                  <path d="M7 14c0 0 1.5 1.5 5 1.5s5-1.5 5-1.5" stroke="rgba(255,255,255,0.4)" stroke-width="1.2" stroke-linecap="round"/>
                </svg>
                <span class="label">GBP Optimization</span>
              </div>
              <p class="feature-desc">Save time, boost revenue and collect 5-star reviews effortlessly.</p>
            </div>
          </div>

          <NuxtLink to="/contact"><button>Contact Us</button></NuxtLink>

          <div class="social-proof">
            <div class="avatars">
              <svg width="148" height="36" viewBox="0 0 148 36" fill="none">
                <circle cx="18" cy="18" r="17" fill="#1e1b4b" stroke="rgba(255,255,255,0.15)" stroke-width="1.5"/>
                <circle cx="18" cy="13" r="5.5" fill="rgba(255,255,255,0.8)"/>
                <ellipse cx="18" cy="27" rx="8" ry="5" fill="rgba(255,255,255,0.8)"/>

                <circle cx="44" cy="18" r="17" fill="#312e81" stroke="rgba(255,255,255,0.15)" stroke-width="1.5"/>
                <circle cx="44" cy="13" r="5.5" fill="rgba(255,255,255,0.8)"/>
                <ellipse cx="44" cy="27" rx="8" ry="5" fill="rgba(255,255,255,0.8)"/>

                <circle cx="70" cy="18" r="17" fill="#7c2d12" stroke="rgba(255,255,255,0.15)" stroke-width="1.5"/>
                <circle cx="70" cy="13" r="5.5" fill="rgba(255,255,255,0.8)"/>
                <ellipse cx="70" cy="27" rx="8" ry="5" fill="rgba(255,255,255,0.8)"/>

                <circle cx="96" cy="18" r="17" fill="#164e63" stroke="rgba(255,255,255,0.15)" stroke-width="1.5"/>
                <circle cx="96" cy="13" r="5.5" fill="rgba(255,255,255,0.8)"/>
                <ellipse cx="96" cy="27" rx="8" ry="5" fill="rgba(255,255,255,0.8)"/>

                <circle cx="122" cy="18" r="17" fill="#1f2937" stroke="rgba(255,255,255,0.15)" stroke-width="1.5"/>
                <text x="122" y="23" text-anchor="middle" fill="rgba(255,255,255,0.7)" font-size="9.5" font-family="Inter" font-weight="500">+5k</text>
              </svg>
            </div>

            <div class="proof-text">
              <span class="count">10,000+</span>
              <span class="label-proof">Positive reviews</span>
            </div>
          </div>

        </div>

        <div class="illustration">
          <img src="@/assets/images/design3.png" alt="">
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
</script>

<style lang="scss" scoped>
div.container {
  padding-top: 200px;

  & div.content {
    box-sizing: border-box;
    max-width: 1920px;
    margin: auto;
    padding: 0 100px;
    display: flex;
    justify-content: space-between;
    align-items: center;

    & div.info {
      width: 50%;

      .eyebrow {
        display: flex;
        align-items: center;
        gap: 8px;
        margin-bottom: 28px;

        span {
          font-family: 'Inter';
          font-size: 12px;
          font-weight: 500;
          letter-spacing: 0.08em;
          text-transform: uppercase;
          color: #FE804B;
        }
      }

      & h2 {
        margin-top: 0;
        margin-bottom: 24px;
        font-family: 'Archivo';
        font-weight: 600;
        font-size: 58px;
        line-height: 68px;
        letter-spacing: -1px;
        color: #FFFFFF;

        @media only screen and (max-width: 450px) {
          font-size: 40px;
          line-height: 50px;
          letter-spacing: -0.75px;
        }
      }

      p.subtitle {
        font-family: 'Inter';
        font-weight: 400;
        font-size: 15px;
        line-height: 25px;
        color: rgba(255, 255, 255, 0.5);
        margin-bottom: 40px;
        max-width: 400px;
      }

      .feature-list {
        margin-bottom: 44px;

        .divider {
          width: 100%;
          height: 1px;
          background: rgba(255, 255, 255, 0.07);
          margin: 0;
        }

        .feature-row {
          display: flex;
          align-items: center;
          gap: 20px;
          padding: 18px 0;

          .feature-left {
            display: flex;
            align-items: center;
            gap: 10px;
            min-width: 170px;
            flex-shrink: 0;

            span.label {
              font-family: 'Inter';
              font-weight: 500;
              font-size: 14px;
              color: #ffffff;
              white-space: nowrap;
            }
          }

          p.feature-desc {
            font-family: 'Inter';
            font-weight: 400;
            font-size: 13.5px;
            line-height: 21px;
            color: rgba(255, 255, 255, 0.42);
            margin: 0;
            padding-left: 20px;
            border-left: 1px solid rgba(255, 255, 255, 0.1);
          }
        }
      }

      & button {
        all: unset;
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
        margin-bottom: 52px;
        cursor: pointer;

        &:hover {
          background-color: #FF9A63;
        }

        @media only screen and (max-width: 450px) {
          width: 100%;
        }
      }

      .social-proof {
        display: flex;
        align-items: center;
        gap: 20px;

        .avatars svg {
          display: block;
        }

        .proof-text {
          display: flex;
          flex-direction: column;
          gap: 1px;

          .count {
            font-family: 'Inter';
            font-weight: 700;
            font-size: 28px;
            line-height: 30px;
            color: #ffffff;
          }

          .label-proof {
            font-family: 'Inter';
            font-weight: 400;
            font-size: 14px;
            color: rgba(255, 255, 255, 0.45);
          }
        }
      }

      @media only screen and (max-width: 1100px) {
        width: 100%;
      }
    }

    & div.illustration {
      width: 50%;
      max-width: 1000px;

      & img {
        width: 100%;
      }

      @media only screen and (max-width: 1100px) {
        width: 100%;
      }
    }

    @media only screen and (max-width: 1100px) {
      flex-direction: column;
    }

    @media only screen and (max-width: 700px) {
      padding: 0 20px;
    }
  }

  @media only screen and (max-width: 700px) {
    padding-top: 100px;
  }
}
</style>
