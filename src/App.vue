<template>
  <div class="main">
    <CardWrapper />
  </div>
</template>

<script>
import CardWrapper from "./components/CardWrapper.vue";

export default {
  name: "App",
  components: {
    CardWrapper,
  },
};
</script>

<style lang="stylus">
@import './styles/main-styles.styl';
</style>
