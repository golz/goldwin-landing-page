<template>
  <div>
    <transition name="fade">
      <div class="home" v-show="true">
        <div class="divider"></div>
        <div class="profile">
          <img alt="goldwin_japar" src="@/assets/avatar.jpg" class="profile__avatar-img">
          <div class="profile__introduction">
            <h3 class="profile__name">goldwin japar</h3>
            <p class="profile__about">
              software development engineer
              <a href="https://www.blibli.com/" target="_blank">@blibli.com</a>
            </p>
            <div class="profile__links">
              <a href="https://github.com/golz">
                <font-awesome-icon :icon="['fab', 'github']"/>
              </a>
              <a href="https://www.linkedin.com/in/goldwin-japar/">
                <font-awesome-icon :icon="['fab', 'linkedin']"/>
              </a>
              <a href="https://www.facebook.com/goldwin.japar/">
                <font-awesome-icon :icon="['fab', 'facebook']"/>
              </a>
              <a href="mailto:goldwin.japar@gmail.com">
                <font-awesome-icon icon="envelope"/>
              </a>
            </div>
          </div>
        </div>
        <div class="divider"></div>
      </div>
    </transition>
    <svg class="waves" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink"
         viewBox="0 24 150 28" preserveAspectRatio="none" shape-rendering="auto">
      <defs>
        <path id="gentle-wave" d="M-160 44c30 0 58-18 88-18s 58 18 88 18 58-18 88-18 58 18 88 18 v44h-352z"/>
      </defs>
      <g class="parallax">
        <use xlink:href="#gentle-wave" x="48" y="0" fill="rgba(0,149,218,0.7)"/>
        <use xlink:href="#gentle-wave" x="48" y="3" fill="rgba(14,179,255,0.5)"/>
        <use xlink:href="#gentle-wave" x="48" y="5" fill="rgba(116,211,255,0.3)"/>
        <use xlink:href="#gentle-wave" x="48" y="7" fill="rgba(218, 243, 255, 0.2)"/>
      </g>
    </svg>
  </div>
</template>

<script src="./js/home.js"></script>

<style lang="scss" scoped>
  @import "~@/assets/scss/utils/variable";
  @import "~@/assets/scss/utils/responsive";

  .home {
    height: 100vh - 20vh;
    display: flex;
    justify-content: center;
    align-items: center;
    user-select: none;
    overflow: hidden !important;
    @include mobile {
      height: 100vh - 7vh;
    }
  }
  .divider {
    height: 1px;
    border-bottom: 1px solid $gray-light-4;
    width: 45%;
    margin: 0 25px;
  }
  .profile {
    display: flex;
    align-items: center;
    justify-content: space-between;
    box-shadow: $shadow;
    padding: 32px;
    border-radius: 16px;
    &__avatar-img {
      height: 140px;
      width: auto;
      border-radius: 50%;
      margin-right: 32px;
      cursor: pointer;
      transition: all .3s ease;
      &:hover {
        box-shadow: 0 0 24px -4px rgba(0, 0, 0, 0.22);
      }
    }

    &__introduction {
      a {
        text-decoration: none;
        color: $blue;
      }
    }

    &__name {
      font-size: $font-size-large;
    }

    &__about {
      color: $gray;
    }

    &__links {
      a {
        color: $blue-light-2;
        font-size: $font-size;

        &:not(:last-child) {
          margin-right: 8px;
        }
      }
    }
  }

  .parallax > use {
    animation: move-forever 25s cubic-bezier(.55, .5, .45, .5) infinite;
  }

  .parallax > use:nth-child(1) {
    animation-delay: -2s;
    animation-duration: 7s;
  }

  .parallax > use:nth-child(2) {
    animation-delay: -3s;
    animation-duration: 10s;
  }

  .parallax > use:nth-child(3) {
    animation-delay: -4s;
    animation-duration: 13s;
  }

  .parallax > use:nth-child(4) {
    animation-delay: -5s;
    animation-duration: 20s;
  }

  @keyframes move-forever {
    0% {
      transform: translate3d(-90px, 0, 0);
    }
    100% {
      transform: translate3d(85px, 0, 0);
    }
  }
</style>
