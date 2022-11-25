<template>
  <li>{{ name }}?!</li>
</template>

<script>
export default {
  props: {
    name: {
      type: String,
      default: "",
    },
  },
};
</script>

<style scoped lang="scss">
/* scoped -> 타 컴포넌트에는 영향을 미치지 않음. */
h1 {
  color: red;
}
</style>
