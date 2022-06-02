<template>
  <div class="wp-circleRandom">
    <div class="circleRandom">
      <img :src="imagen" alt="dice" />
    </div>
  </div>
</template>

<script>
export default {
  name: "BtnRandom",
  props: {
    imagen: String,
  },
};
</script>
