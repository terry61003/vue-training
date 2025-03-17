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
  <hr>
  <button @click="show('tab1')">Component1</button>
  <button @click="show('tab2')">Component2</button>
  <button @click="show('tab3')">Component3</button>

  <Component1Test v-if="tab === 'tab1'" />
  <Component2Test v-if="tab === 'tab2'" />
  <Component3Test v-if="tab === 'tab3'" />
</template>

<script>
import Header from './components/HeaderTest.vue';
import View from './components/ViewTest.vue';
import InputTest from './components/InputTest.vue';
import CardTest from './components/CardTest.vue';
import CardTest2 from './components/CardTest2.vue';
import Component1Test from './components/Component1Test.vue';
import Component2Test from './components/Component2Test.vue';
import Component3Test from './components/Component3Test.vue';

export default {
  name: 'App',
  components: {
    Header, View, InputTest, CardTest, CardTest2, Component1Test, Component2Test, Component3Test,
  },
  data() {
    return {
      name: 'Allan',
      text: '',
      name2: '',
      tab: 'tab1',
    };
  },
  methods: {
    getViewText(text) {
      this.text = text;
    },
    show(index) {
      this.tab = index;
    },
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
