<template>
  <ComponentDemo :name="name" @getName="getName" />
</template>

<script>
import { ref } from 'vue'
import ComponentDemo from './components/ComponentDemo.vue'

export default {
  name: 'App',
  components: {
    ComponentDemo,
  },
  setup() {
    const name = ref('Jake');

    function getName(value) {
      alert(value)
    }

    return {
      name,
      getName,
    }
  }
}
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
