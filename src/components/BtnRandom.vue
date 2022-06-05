<template>
  <button class="circleRandom" @click="button">
    <img :src="imagen" alt="dice" />
  </button>
</template>

<script>
export default {
  name: "BtnRandom",
  props: ["imagen", "button"],
};
</script>
