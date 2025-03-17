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
  <hr>
  <CardTest>
    <h2>Content</h2>
  </CardTest>
  <CardTest>
    <a href="">Link</a>
  </CardTest>
  <hr>
  <CardTest2>
    <template v-slot:header>
      <h1>My Header</h1>
    </template>
  </CardTest2>
</template>

<script>
import Header from './components/HeaderTest.vue';
import View from './components/ViewTest.vue';
import InputTest from './components/InputTest.vue';
import CardTest from './components/CardTest.vue';
import CardTest2 from './components/CardTest2.vue';

export default {
  name: 'App',
  components: {
    Header, View, InputTest, CardTest, CardTest2
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
