<template>
  <div id="app">
    <img class="bg-img" draggable="false" src="/static/background.png"/>
    <div class="main-container">
      <div class="logo-box">
        <p class="logo">VolatileByte</p>
        <p class="slogan">Game addicts doing dev.</p>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'app'
  }
</script>

<style lang="stylus">

  @import "style/colors.styl"
  @import "style/sizes.styl"
  body, html {
    margin: 0px;
    width: 100%;
    height: 100%;
    overflow: hidden;
  }

  #app {
    width: 100%;
    height: 100%;
    position: relative;
  }

  .bg-img {
    width: 100%;
    z-index: -1;
    position: absolute;
  }

  .main-container {
    height: 100%;
    width: 100%;
    background-color: transparent;
  }

  .logo-box {
    p {
      line-height: 32px;
      font-family: Arial;
      margin: 0px;
    }

    .logo {
      font-size: $font-size-l;
      color: rgb(244, 244, 244);
      text-shadow: rgb(255, 255, 255) 0px -1px 4px, rgb(255, 255, 0) 0px -2px 10px, rgb(255, 128, 0) 0px -10px 20px, rgb(255, 0, 0) 0px -18px 40px;
    }

    .slogan {
      font-size: $font-size-s;
      color: rgb(244, 244, 244);
      text-shadow: rgb(255, 255, 255) 0px -1px 4px, rgb(255, 255, 0) 0px -2px 10px, rgb(255, 128, 0) 0px -10px 20px, rgb(255, 0, 0) 0px -18px 40px;
    }
  }

  @media screen and (max-width: 1110px) {
    .bg-img {
      width: 1110px;
      margin-left: 50%;
      transform: translateX(-50%);
    }
  }

  @media screen and (max-aspect-ratio: 1 / 1) {
    .main-container {
      display: flex;
      justify-content: center;
    }

    .logo-box {
      margin-top: 96px;
    }
  }

  @media screen and (min-aspect-ratio: 1 / 1) {
    .logo-box {
      position: absolute;
      bottom: 48px;
      right: 48px;
    }
  }

</style>
