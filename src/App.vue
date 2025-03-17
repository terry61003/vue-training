<template>
  <p>{{ count }}</p>
  <button @click="incrementCount">button</button>
  <hr>
  {{ name }}
  <br>
  <input type="text" v-model="name" />
  <hr>
  {{ email }}
  <br>
  <input type="text" v-model="email" />
</template>

<script>
import { ref, reactive, toRefs } from 'vue';

export default {
  name: 'App',
  setup() {
    const count = ref(0);
    const name = ref('');
    const user = reactive({
      email: '',
    });
    
    function incrementCount() {
      count.value++;
    }
    
    return {
      count,
      incrementCount,
      name,
      ...toRefs(user),
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
