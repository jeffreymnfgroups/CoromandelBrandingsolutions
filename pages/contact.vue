<template>
  <div class="contact-page">
    <div class="hero-container">
      <div class="content">
        <h1 class="heading">Get in <img class="mail" src="@/assets/images/mail.png" alt=""> <br> 
          <img src="@/assets/images/arrows.svg" alt=""> touch with us
        </h1>
        <p class="subheading">Have a project in mind? We'd love to hear from you. <br>
          Fill out the form below and we'll get back to you shortly.
        </p>

        <form class="contact-form" @submit.prevent="handleSubmit">
          <div class="form-group">
            <input type="text" placeholder="Your Name" required />
          </div>
          <div class="form-group">
            <input type="email" placeholder="Your Email" required />
          </div>
          <div class="form-group">
            <textarea placeholder="Your Message" rows="5" required></textarea>
          </div>
          <button type="submit" class="contact-cta">Send Message</button>
        </form>
      </div>
      <img class="wave" src="@/assets/images/wave2.svg" alt="">
    </div>
  </div>
</template>

<script setup>
const handleSubmit = () => {
  alert('Thank you for your message! (In a real app, this would be sent to a server)');
};
</script>

<style lang="scss" scoped>
div.contact-page {
  background-color: #ECEADD;
  min-height: 100vh;
}

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

      @media only screen and (max-width: 1100px) {
        font-size: 68px;
        line-height: 100%;
        & img { width: 68px !important; }
      }

      @media only screen and (max-width: 700px) {
        font-size: 48px;
        & img { width: 48px !important; }
      }

      @media only screen and (max-width: 450px) {
        font-size: 36px;
        & img { width: 34px !important; }
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
      margin-bottom: 40px;
    }

    & form.contact-form {
      max-width: 600px;
      display: flex;
      flex-direction: column;
      gap: 20px;

      & .form-group {
        width: 100%;
        & input, & textarea {
          width: 100%;
          padding: 16px;
          border-radius: 12px;
          border: 1px solid rgba(24, 50, 130, 0.2);
          background-color: white;
          font-family: 'Inter';
          font-size: 16px;
          color: #183282;
          box-sizing: border-box;

          &:focus {
            outline: none;
            border-color: #FE804B;
          }
        }
      }

      & button.contact-cta {
        all: unset;
        width: 200px;
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

        @media only screen and (max-width: 450px) {
          width: 100%;
        }
      }
    }

    @media only screen and (max-width: 1100px) {
      padding: 0 40px;
      padding-bottom: 100px;
    }
  }

  & img.wave {
    position: absolute;
    top: 220px;
    right: 100px;
    z-index: -1;
    opacity: 0.5;

    @media only screen and (max-width: 1100px) {
      scale: .8;
      right: 0px;
    }
  }

  @media only screen and (max-width: 700px) {
    padding-top: 120px;
  }
}
</style>
