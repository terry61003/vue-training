<template>
  <Header :name="name" />
  <hr>
  <View @view-text="getViewText" />
  <br>
  {{ text }}
</template>

<script>
import Header from './components/HeaderTest.vue';
import View from './components/ViewTest.vue';

export default {
  name: 'App',
  components: {
    Header, View
  },
  data() {
    return {
      name: 'Allan',
      text: '',
    };
  },
  methods: {
    getViewText(text) {
      this.text = text;
    }
  }
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
