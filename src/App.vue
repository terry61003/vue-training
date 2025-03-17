<template>
  {{ name }}
  <br>
  {{ user.id }} {{ user.name }}
</template>

<script>
import { ref, reactive } from 'vue';

export default {
  name: 'App',
  setup() {
    const name = ref('');
    const user = reactive({
      id: 0,
      name: '',
    });

    // 設定值要使用value
    name.value = 'Jake';

    user.id = 1;
    user.name = 'Allan';

    return {
      name, user
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
