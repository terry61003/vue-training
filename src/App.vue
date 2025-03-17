<template>
  {{ name }}
  <br>
  <input type="text" v-model="name">
  <br>
  <input type="text" v-model.trim="name">
  <br>
  <input type="text" v-model.lazy="name">
  <hr>
  <p v-once>{{ message }}</p>
  <input type="text" v-model="message" />
  <hr>
  <p v-pre>{{ name }}</p>
  <input type="text" v-model="name" />
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      name: '',
      message: 'Hello',
    };
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
