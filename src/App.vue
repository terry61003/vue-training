<template>
  {{ count }}
  <br />
  <button @click="addCount">Add Count</button>
  <hr>
  <input type="text" v-model="user.name" />
  <hr>
  <button @click="addItem">Add item</button>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      count: 0,
      user: {
        name: '',
      },
      items: [],
    };
  },
  methods: {
    addCount() {
      this.count += 1;
    },
    addItem() {
      this.items.push('test');
    },
  },
  watch: {
    count(newValue, oldValue) {
      console.log(newValue, oldValue);
    },
    user: {
      handler(newValue) {
        console.log(newValue);
      },
      deep: true, //要監聽物件時，要設定才會起作用
    },
    items: {
      handler(newValue) {
        console.log(newValue);
      },
      deep: true, //要監聽陣列時，要設定才會起作用
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
