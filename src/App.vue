<template>
  <div class="main">
    <CardWrapper
      frase="It is easy to sit up ad take notice, what's difficult is getting up and
        taking action."
    />
  </div>
</template>

<script>
import CardWrapper from "./components/CardWrapper.vue";

export default {
  name: "App",
  components: {
    CardWrapper,
  },
  methods: {
    getFrase() {
      console.log("API --> https://api.adviceslip.com/advice");
    },
  },
};
</script>

<style lang="stylus">
@import './styles/main-styles.styl';
</style>
