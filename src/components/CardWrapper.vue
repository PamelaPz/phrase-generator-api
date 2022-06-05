<template>
  <div class="card">
    <section class="wp-text">
      <h4 class="title-mini">
        Advice <span>#{{ number }}</span>
      </h4>
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
    <div class="wp-circleRandom">
      <BtnRandom :imagen="img_src" :button="getFrase" />
    </div>
  </div>
</template>

<script>
import axios from "axios";
import BtnRandom from "./BtnRandom.vue";
import dice from "@/assets/images/icon-dice.svg";

export default {
  name: "wp-card",
  data() {
    return {
      img_src: dice,
      number: 117,
      frase:
        "It is easy to sit up ad take notice, what's difficult is getting up and taking action.",
    };
  },
  components: {
    BtnRandom,
  },
  methods: {
    getFrase() {
      axios
        .get("https://api.adviceslip.com/advice")
        .then((response) => {
          let phase = response.data.slip.advice;
          let id = response.data.slip.id;

          this.frase = phase;
          this.number = id;
        })
        .catch((error) => console.log(error));
    },
  },
};
</script>
