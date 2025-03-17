<template>
  <Header :name="name" />
</template>

<script>
import Header from './components/HeaderTest.vue';

export default {
  name: 'App',
  components: {
    Header,
  },
  data() {
    return {
      name: 'Allan',
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
