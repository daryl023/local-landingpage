<template>
  <div class="starters limiter">
    <div class="container position-lift">
      <div class="anim anim__first card card--dark">
        <h2>iOS</h2>
        <span>Compatible with iPhone, iPad, Apple Watch</span>
      </div>
      <div class="anim anim__sec card card--dark">
        <h2>Android</h2>
        <span>Operates in Phone, Tablet, Smartwatch</span>
      </div>
      <div class="anim anim__third card card--dark">
        <h2>Web</h2>
        <span>Runs everywhere in the web</span>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  components: {},
};
</script>
<style lang="scss" scoped>
.starters {
  width: 100%;
  margin-inline: auto;
  color: var(--primary);
}

.card {
  &--dark {
    background: rgb(20, 38, 42, 0.5) !important;
    border: none !important;
    backdrop-filter: blur(16px);
  }
}
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
    "anim__first"
    "anim__sec"
    "anim__third";
  // transform: scale(0.88);
  padding-inline: var(--step-4);
  padding-block: var(--step-0);
}
.anim {
  height: max-content;
}

.anim__first {
  grid-area: anim__first;
}

.anim__sec {
  grid-area: anim__sec;
}

.anim__third {
  grid-area: anim__third;
}

.anim {
  justify-content: center;
  h2 {
    font-size: var(--step-0);
  }

  span {
    line-height: var(--step-0);
    color: var(--primary);
    font-size: var(--step--4);
  }
}

@media (min-width: 980px) {
  .container {
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: 1fr;
    grid-template-areas: "anim__first anim__sec anim__third";
  }

  .anim {
    height: 100%;
  }
}
</style>
