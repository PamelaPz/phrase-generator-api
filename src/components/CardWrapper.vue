<template>
  <div class="card">
    <section class="wp-text">
      <h4 class="title-mini">Advice <span>#117</span></h4>
      <h2>"{{ frase }}"</h2>
      <div class="separator">
        <img
          class="hidden-mobile show-desktop"
          src="@/assets/images/pattern-divider-desktop.svg"
          alt="divider"
        />
        <img
          class="hidden-desktop show-mobile"
          src="@/assets/images/pattern-divider-mobile.svg"
          alt=""
        />
      </div>
    </section>
    <BtnRandom :imagen="img_src" />
  </div>
</template>

<script>
import BtnRandom from "./BtnRandom.vue";
import dice from "@/assets/images/icon-dice.svg";

export default {
  name: "wp-card",
  props: {
    frase: String,
  },
  data() {
    return {
      img_src: dice,
    };
  },
  components: {
    BtnRandom,
  },
};
</script>
