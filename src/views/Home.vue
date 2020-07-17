<template>
  <transition name="fade">
    <div class="home" v-show="true">
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
              <font-awesome-icon :icon="['fab', 'github']" />
            </a>
            <a href="https://www.linkedin.com/in/goldwin-japar/">
              <font-awesome-icon :icon="['fab', 'linkedin']" />
            </a>
            <a href="https://www.facebook.com/goldwin.japar/">
              <font-awesome-icon :icon="['fab', 'facebook']" />
            </a>
            <a href="mailto:goldwin.japar@gmail.com">
              <font-awesome-icon icon="envelope" />
            </a>
          </div>
        </div>
      </div>
    </div>
  </transition>
</template>

<script src="./js/home.js"></script>

<style lang="scss" scoped>
  @import "~@/assets/scss/utils/variable";

  .home {
    height: 600px;
    display: flex;
    justify-content: center;
    align-items: center;
    user-select: none;
  }
  .profile {
    display: flex;
    align-items: center;
    justify-content: space-between;
    &__avatar-img {
      height: 150px;
      width: auto;
      border-radius: 50%;
      margin-right: 32px;
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
</style>
