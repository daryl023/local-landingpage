<script>
import LottieAnimation from "lottie-web-vue";

export default {
  data() {
    return {
      mobile: null,
      mobileNav: null,
      windownWidth: null,
    };
  },
  created() {
    window.addEventListener("resize", this.checkScreen);
  },
  destroyed() {
    window.addEventListener("resize", this.checkScreen);
  },
  components: {
    LottieAnimation,
  },
  methods: {
    checkScreen() {
      this.windownWidth = window.innerWidth;
      if (this.windownWidth <= 950) {
        this.mobile = true;
        return;
      }
      this.mobile = false;
      this.mobileNav = false;
      return;
    },
    toggleMobileNav() {
      this.mobileNav = !this.mobileNav;
    },
  },
  mounted() {
    this.checkScreen();
  },
};
</script>
<template>
  <main class="hero limiter position-lift" id="parent_hero">
    <div
      class="hero position-lift"
      style="padding-top: clamp(8.84rem, calc(2.34rem + 9.12vw), 4.17rem)"
    >
      <lottie-animation
        style="transform: scale(0.88); height: 100%; margin-bottom: -2rem"
        :animationData="require('@/assets/hero-text.json')"
        :loop="true"
      />
      <div class="hero__lead animate-lead">
        <p>
          Bring your websites and apps to life with the <br />
          <strong> simplest editor for lottie animations </strong>
        </p>
      </div>
      <div class="button">
        <button class="button__beta animate-lead">Get early access</button>
      </div>
    </div>
  </main>
</template>

<style lang="scss" scoped>
main {
  align-items: center;
  display: flex;
  flex-direction: column;
  gap: var(--step-0);
  height: 100%;
  padding-inline: var(--step-4);
  padding-block: var(--step-0);
  justify-content: center;
  text-align: center;
  overflow-x: hidden;
  margin-inline: auto;

  @media (max-height: 593px) {
    margin-top: 10em;
  }
  .hero {
    align-items: center;
    display: flex;
    flex-direction: column;
    gap: 48px;
    width: 100%;

    h1 {
      font-size: var(--step-2);
      line-height: var(--step-4);
      width: 80%;
    }
    &--highlight {
      background: linear-gradient(
        150deg,
        var(--teal) 0%,
        rgba(98, 122, 246, 1) 100%
      );
      background-size: 200%;
      right: 0;
      left: 100%;
      background-clip: text;
      -webkit-text-fill-color: transparent;
      -webkit-background-clip: text;
    }
    &__lead {
      width: clamp(18.75rem, 12.41rem + 31.71vw, 35rem);
      font-weight: var(--normal);
      font-size: clamp(0.5rem, calc(0.21rem + 1.46vw), 1.25rem);
      line-height: var(--step-0);
      color: #5c617c;
    }
  }

  .button {
    display: flex;
    flex-direction: column;
    gap: var(--step-0);
    position: relative;
    padding: 4px;
    transition: all 200ms ease-out;
    border-radius: var(--step--1);

    &:hover,
    &:focus-visible {
      transform: scale(0.96);
    }

    &:active {
      transform: scale(0.85);
    }

    button {
      border-radius: inherit;
      font-size: var(--step--3);
      line-height: var(--step-0);
      padding-block: var(--step--3);
      padding-inline: var(--step-1);
      transform: none !important;
    }

    &:after {
      content: "";
      height: inherit;
      background-image: linear-gradient(
        79.84deg,
        rgb(122, 111, 251, 0.5) -1%,
        rgb(255, 84, 103, 0.5) 88%,
        rgb(253, 190, 4, 0.5) 100%
      );
      position: absolute;
      z-index: -1;
      top: 0;
      right: 0;
      left: 0;
      bottom: 0;
      border-radius: inherit;
    }
    &__beta {
      background-image: linear-gradient(
        79.84deg,
        #7a6ffb -1%,
        #ff5467 88%,
        #fdbe04 132%
      );
      color: #ffffff;

      &:hover {
        -webkit-box-shadow: 3px 1px 15px 0px rgb(48, 165, 173, 0.25);
        -moz-box-shadow: 3px 1px 15px 0px rgb(48, 165, 173, 0.25);
        box-shadow: 3px 1px 15px 0px rgb(48, 165, 173, 0.25);
      }
    }
  }
}
@media (min-width: 980px) {
  main {
    .button {
      display: flex;
      flex-direction: row;
    }
  }
}
</style>
