<template>
  <section class="hero-component"
  :style="{ backgroundImage: `url(${backgroundUrl})` }">
    <div class="overlay"></div>
    <h1 class="title">{{ title }}</h1>
    <p class="sub-title">{{ subTitle }}</p>
    <button class="button" type="button" name="button">{{ btnText }}</button>
  </section>
</template>

<script>

export default {
  props: {
    title: {
      type: String,
      default: 'Dope Nuxt.js Theme'
    },
    subTitle: {
      type: String,
      default: 'A Theme Built By Elliot Richardson'
    },
    backgroundUrl: {
      type: String,
      default: require('~/assets/building1.jpg')
    },
    btnText: {
      type: String,
      default: 'Sign Up Now'
    }

  },
  data() {
    return {}
  }
}
</script>

<style lang="scss" scoped>
@import '~assets/scss/variables.scss';

  .hero-component {
    position: relative;
    height: 500px;
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    box-sizing: border-box;
    color: $white;

    &.hero-component--light {
      color: $white;
    }

    &.hero-component--dark {
      color: $black;
    }

    .overlay {
      height: 500px;
      width: 100%;
      position: absolute;
      top: 0;
      left: 0;
      background-image: linear-gradient(45deg, rgba(0,0,0,.3), rgba(0,0,0,.3));
    }

    .title {
      font-size: 60px;
      z-index: 1;
    }

    .sub-title {
      margin-bottom: 40px;
      font-size: 16px;
      z-index: 1;
    }

    .button {
      z-index: 1;
      background: #00BCD4;
      border: none;
      padding: 10px 25px;
      border-radius: $radius;
      color: white;
      box-shadow: 0 4px 8px rgba(0,0,0,.1)
    }
  }


</style>
