<!-- HTML -->
<template>
  <div class="plus" @click="increase()">+</div>
  <h1>{{ count }}</h1>
  <div class="minus" @click="decrease()">-</div>

  <div v-if="count > 4">4보다 큼!</div>

  <ul>
    <fruit v-for="fruit in fruits" :key="fruit" :name="fruit">
      {{ fruit }}
    </fruit>
  </ul>
</template>

<!-- JS / TS -->
<script>
import Fruit from "./components/Fruit.vue";

export default {
  components: {
    fruit: Fruit,
  },
  data() {
    return {
      count: 0,
      fruits: ["Apple", "Banana", "Cherry"],
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
<style lang="scss">
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

ul {
  li {
    font-size: 30px;
    font-weight: 700;
    list-style: none;
  }
}
</style>
