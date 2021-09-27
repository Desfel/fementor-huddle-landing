<template>
  <div class="page-wrapper">
      <img class="huddle-logo" src="@/assets/img/logo.svg" alt="Huddle" />

    <div class="page-content">
      <div class="img-wrapper">
        <img
          class="huddle-img"
          src="@/assets/img/illustration-mockups.svg"
          alt="Mockups"
        />
      </div>

      <div class="main-content">
        <h1>
          Build The Community Your Fans Will Love
        </h1>

        <p>
          Huddle re-imagines the way we build communities. You have a voice, but so does your audience.
          Create connections with your users as you engage in genuine discussion.
        </p>

        <a href="#">Register</a>
      </div>
    </div>

    <div class="socials-wrapper">
      <a class="social-btn facebook" href="#">
        <i class="icon-facebook"></i>
      </a>
      <a class="social-btn twitter" href="#">
        <i class="icon-twitter"></i>
      </a>
      <a class="social-btn instagram" href="#">
        <i class="icon-instagram"></i>
      </a>
    </div>
  </div>
</template>

<script>
import { mapState } from 'vuex'

export default {
  head() {
    return {
      title: {
        inner: 'Home'
      },
      meta: [
        {
          name: 'description',
          content: `${this.appTitle} home page`,
          id: 'desc'
        }
      ]
    }
  },
  computed: mapState('app', ['appTitle'])
}
</script>

<style lang="scss" scoped>
@import '@/theme/variables.scss';

.page-wrapper {
  display: flex;
  flex-direction: column;
  align-items: flex-start;

  .huddle-logo {
    align-self: flex-start;

    @media (max-width: 768px) {
      width: 120px;
    }
  }
}

.page-content {
  display: flex;
  margin: 104px 0 27px;
  min-width: 0;

  @media (max-width: 768px) {
    flex-direction: column;
    justify-content: center;
    margin-top: 60px;
  }

  .img-wrapper {
    width: 60%;
    margin-right: 60px;

    @media (max-width: 768px) {
      margin-right: 0;
      width: 100%;
    }
  }

  .huddle-img {
    width: 100%;
    height: auto;
  }
}

.main-content {
  margin-top: 32px;
  width: 40%;

  @media (max-width: 768px) {
    width: 100%;
    margin: 60px auto 64px;
    text-align: center;
  }

  h1 {
    font-family: $headingText;
    font-weight: 600;
    font-size: 40px;
    line-height: 60px;
    color: $light;

    @media (max-width: 1024px) {
      font-size: 24px;
      line-height: 36px;
    }
  }

  p {
    margin: 24px 0;
    font-family: $textFont;
    font-weight: normal;
    font-size: 18px;
    line-height: 27px;
    color: $light;

    @media (max-width: 1024px) {
      margin: 16px 0 24px;
      font-size: 16px;
      line-height: 24px;
    }
  }

  a {
    display: inline-block;
    padding: 13px 64px 16px;

    font-family: $headingText;
    font-style: normal;
    font-weight: normal;
    font-size: 18px;
    line-height: 27px;
    color: $primaryColor1;

    background: $light;
    box-shadow: 2px 4px 9px 3px rgba(0, 0, 0, 0.258633);
    border-radius: 28px;

    transition: all .3s ease-in-out;

    @media (max-width: 768px) {
      padding: 11px 75px;
      font-size: 12px;
      line-height: 18px;
    }

    &:hover {
      background: $primaryColor2;
      color: $light;
    }
  }
}

.socials-wrapper {
  display: flex;
  align-items: center;
  margin-left: auto;

  @media (max-width: 768px) {
    margin: auto;
  }

  .social-btn {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 31px;
    height: 31px;
    border-radius: 50%;
    border: 1px solid $light;
    transition: border-color .3s ease-in-out;


    &:not(:last-child) {
      margin-right: 13px;
    }

    &:hover {
      border-color: $hoverColor;

      i {
        color: $hoverColor;
      }
    }

    i {
      color: $light;
      transition: color .3s ease-in-out;
    }
  }
}


[class^="icon-"], [class*=" icon-"] {
  /* use !important to prevent issues with browser extensions that change fonts */
  font-family: 'icomoon' !important;
  speak: never;
  font-style: normal;
  font-weight: normal;
  font-variant: normal;
  text-transform: none;
  line-height: 1;

  /* Better Font Rendering =========== */
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.icon-facebook:before {
  content: "\ea90";
}
.icon-instagram:before {
  content: "\ea92";
}
.icon-twitter:before {
  content: "\ea96";
}
</style>
