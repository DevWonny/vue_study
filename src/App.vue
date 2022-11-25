<!-- HTML -->
<template>
  <div class="plus" @click="increase()">+</div>
  <h1>{{ count }}</h1>
  <div class="minus" @click="decrease()">-</div>
</template>

<!-- JS / TS -->
<script>
export default {
  data() {
    return {
      count: 0,
    };
  },
  methods: {
    increase() {
      this.count += 1;
    },
    decrease() {
      this.count -= 1;
    },
  },
};
</script>

<!-- CSS / SCSS -->
<style>
h1 {
  font-size: 50px;
  color: royalblue;
  margin: 0;
}
.plus,
.minus {
  cursor: pointer;
  font-size: 30px;
  width: 300px;
  height: 50px;
  border: 1px solid #000;
  text-align: center;
  line-height: 50px;
}
</style>
