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
  <hr>
  {{ text }} <br />
  <textarea v-model="text" />
  <hr>
  {{ selectValue }} <br />
  <select v-model="selectValue">
    <option value="">select</option>
    <option value="1">1</option>
    <option value="2">2</option>
    <option value="3">3</option>
  </select>
  <hr>
  {{ isCheck }} <br />
  <input type="checkbox" v-model="isCheck" /> is check
  <hr>
  {{ checkbox }} <br />
  <input type="checkbox" value="0" v-model="checkbox" /> 0
  <input type="checkbox" value="1" v-model="checkbox" /> 1
  <input type="checkbox" value="2" v-model="checkbox" /> 2
  <input type="checkbox" value="3" v-model="checkbox" /> 3
  <hr>
  {{ radio }} <br />
  <input type="radio" value="0" v-model="radio" /> 0
  <input type="radio" value="1" v-model="radio" /> 1
  <input type="radio" value="2" v-model="radio" /> 2
  <input type="radio" value="3" v-model="radio" /> 3
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      name: '',
      message: 'Hello',
      text: '',
      selectValue: '',
      isCheck: false,
      checkbox: [],
      radio: '',
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
