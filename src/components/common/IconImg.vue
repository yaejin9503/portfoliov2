<template>
  <div class="img-container">
    <div class="img-wrap">
      <img :src="src" />
    </div>
    <span>{{ title }}</span>
  </div>
</template>
<script>
export default {
  props: {
    src: {
      type: String,
    },
    title: {
      type: String,
    },
  },
};
</script>
<style scoped>
span {
  display: block;
  text-align: center;
}
img {
  width: 100%;
}
</style>
