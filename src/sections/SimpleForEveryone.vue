<template>
  <div class="simple-for-everyone position-lift limiter-width">
    <section class="wrapper">
      <div class="title" id="about">
        <div class="container">
          <div class="first__col__title">
            <div class="section__title">
              <h1>Simple for everyone</h1>
              <span>
                New to product animations or know your <br />
                way around - no worries.</span
              >
              <button class="full">
                Get Started
                <icon name="arrow" class="arrow" />
              </button>
            </div>
          </div>
          <div class="section__cards">
            <div class="card card--light card--shadow box box__ditch">
              <h2>Ditch the learning curve</h2>
              <span
                >We keep it simple, so you’re free to create powerful results - no After
                Effects qualifications needed.</span
              >
            </div>
            <div class="card card--light card--shadow box box__fun">
              <h2>Have fun in the browser</h2>
              <span
                >With an entirely web-based editor and workflow, access your work from any
                device and forget downloading large apps and files.</span
              >
            </div>
          </div>
        </div>
      </div>
      <div class="scroll">
        <div class="roles">
          <div class="container">
            <div class="role__designer card card--light card--shadow">
              <div class="role__container">
                <div class="profile__container">
                  <lottie-vue-player
                    :src="`https://assets7.lottiefiles.com/private_files/lf30_tvnnnk4i.json`"
                    class="profile__animation"
                  />
                </div>
                <div class="profile__details">
                  <h2>Designers</h2>
                  <span
                    >withLottieLab Edit illustrations and micro-interactions without
                    needing to disturb a designer.</span
                  >
                </div>
              </div>
            </div>
            <div class="role__developer card card--light card--shadow">
              <div class="role__container">
                <div class="profile__container">
                  <lottie-vue-player
                    :src="`https://assets7.lottiefiles.com/private_files/lf30_tvnnnk4i.json`"
                    class="profile__animation"
                  />
                </div>
                <div class="profile__details">
                  <h2>Designers</h2>
                  <span
                    >withLottieLab Edit illustrations and micro-interactions without
                    needing to disturb a designer.</span
                  >
                </div>
              </div>
            </div>
            <div class="role__project-manager card card--light card--shadow">
              <div class="role__container">
                <div class="profile__container">
                  <lottie-vue-player
                    :src="`https://assets7.lottiefiles.com/private_files/lf30_tvnnnk4i.json`"
                    class="profile__animation"
                  />
                </div>
                <div class="profile__details">
                  <h2>Designers</h2>
                  <span
                    >withLottieLab Edit illustrations and micro-interactions without
                    needing to disturb a designer.</span
                  >
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import icon from "@/assets/Icons.vue";
// import LottieAnimation from "lottie-web-vue";

export default {
  name: "SimpleForEveryone",
  data() {
    return {
      controller: null,
      tween: null,
      scene: null,
    };
  },
  components: {
    icon,
    // LottieAnimation,
  },
};
</script>

<style lang="scss" scoped>
.simple-for-everyone {
  margin: 0 auto;
  padding: 0;

  .wrapper {
    display: flex;
    flex-direction: column;
    // transform: scale(0.88);
    padding-inline: var(--step-4);
    padding-block: var(--step-0);
    margin: auto;
    gap: var(--step-1);
    .title {
      display: flex;
      justify-content: center;
      align-items: center;

      .container {
        display: grid;
        grid-template-columns: 1fr;
        grid-template-rows: min-content;
        grid-auto-columns: 1fr;
        grid-auto-rows: 1fr;
        gap: 32px 32px;
        grid-auto-flow: row;
        justify-items: stretch;
        grid-template-areas:
          "first__col__title"
          "section__cards";
        margin-inline: auto;
        justify-content: center;
        height: 100%;
        align-items: end;
      }

      .section__cards {
        display: grid;
        grid-template-columns: 1fr;
        grid-template-rows: 1fr 1fr;
        gap: 32px 32px;
        grid-auto-flow: row;
        grid-template-areas:
          "card__ditch"
          "card__fun";
        grid-area: section__cards;
      }
      .card {
        padding: var(--step-2) !important;
      }
      .box {
        display: flex;
        justify-content: center;
        h2 {
          font-size: var(--step--1);
        }
        span {
          font-size: var(--step--4);
          line-height: var(--step-0);
        }
        &__ditch {
          grid-area: card__ditch;
        }
        &__fun {
          grid-area: card__fun;
        }
      }

      .first__col__description {
        grid-area: first__col__description;
      }

      .first__col__title {
        grid-area: first__col__title;

        .section__title {
          span {
            line-height: var(--step-0);
          }
          button {
            gap: var(--step--4);
            align-items: center;
            height: max-content;
            color: var(--purple);

            .arrow {
              display: flex;
              stroke: var(--purple);
            }
          }
        }
      }
    }

    .scroll {
      display: flex;
      flex-direction: column;
      gap: var(--step-0);
      justify-content: center;

      .container {
        display: grid;
        grid-template-columns: 1fr;
        grid-template-rows: 1fr 1fr 1fr;
        grid-auto-columns: 1fr;
        grid-auto-rows: 1fr;
        gap: 32px 32px;
        grid-auto-flow: row;
        justify-items: stretch;
        grid-template-areas:
          "role__designer"
          "role__developer"
          "role__project-manager";
        // height: 100%;
        // width: 84%;
        margin-inline: auto;
        justify-content: center;
      }

      .role__project-manager {
        grid-area: role__project-manager;
        border: solid var(--teal) 4px;
        .profile__container {
          background: var(--teal);
        }
      }

      .role__developer {
        grid-area: role__developer;
        border: solid var(--purple) 4px;
        .profile__container {
          background: var(--purple);
        }
      }

      .role__designer {
        grid-area: role__designer;
        border: solid var(--blue) 4px;
        .profile__container {
          background: var(--blue);
        }
      }
      .role__container {
        display: flex;
        gap: var(--step-0);
        align-items: center;
        height: 100%;

        .profile__container {
          width: var(--step-7);
          height: fit-content;
          display: flex;
          flex-wrap: wrap;
          border-radius: var(--step-0);
          .profile__animation {
            margin: 0;
            padding: 0;
            aspect-ratio: 1 / 1;
          }
        }
        .profile__details {
          width: 80%;
          height: 100%;
          justify-content: space-evenly;
          display: flex;
          flex-direction: column;

          h2 {
            font-size: var(--step--1);
          }
          span {
            font-size: var(--step--4);
            line-height: var(--step--2);
          }
        }
      }
    }
  }
}

@media (min-width: 980px) {
  .simple-for-everyone {
    margin: 0 auto;
    padding: 0;
    // height: 100vh;
    display: flex;
    justify-content: center;

    .wrapper {
      display: flex;
      flex-direction: row;
      margin: auto;
      gap: var(--step-0);

      .title {
        display: flex;
        justify-content: center;
        align-items: center;
        width: 50%;
        position: sticky;
        position: -webkit-sticky;
        top: 0;

        .container {
          display: grid;
          grid-template-columns: 1fr;
          grid-template-rows: min-content;
          grid-auto-columns: 1fr;
          grid-auto-rows: 1fr;
          grid-auto-flow: row;
          justify-items: stretch;
          grid-template-areas:
            "first__col__title"
            "section__cards";
          width: 100%;
          margin: 0;
        }

        .section__cards {
          display: grid;
          grid-template-columns: 1fr 1fr;
          grid-template-rows: 1fr 1fr 1fr;
          gap: 0px 32px;
          grid-auto-flow: row;
          grid-template-areas:
            "card__ditch card__fun"
            "card__ditch card__fun"
            "card__ditch card__fun";
          grid-area: section__cards;
        }
      }

      .scroll {
        width: 50%;

        .container {
          display: grid;
          grid-template-columns: 1fr;
          grid-template-rows: 1fr 1fr 1fr;
          grid-auto-columns: 1fr;
          grid-auto-rows: 1fr;
          grid-auto-flow: row;
          justify-items: stretch;
          grid-template-areas:
            "role__designer"
            "role__developer"
            "role__project-manager";
          width: 75%;
        }
      }
    }
  }
}
</style>
