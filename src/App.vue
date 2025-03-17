<template>
  <Header :name="name" />
  <hr>
  <View @view-text="getViewText" />
  <br>
  {{ text }}
  <hr>
  <InputTest v-model="name2" />
  <br>
  {{ name2 }}
</template>

<script>
import Header from './components/HeaderTest.vue';
import View from './components/ViewTest.vue';
import InputTest from './components/InputTest.vue';

export default {
  name: 'App',
  components: {
    Header, View, InputTest
  },
  data() {
    return {
      name: 'Allan',
      text: '',
      name2: '',
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
