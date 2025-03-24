<template>
  <div class="about">
    <h1>This is an about page</h1>
    <h1>{{ x }}</h1>
    <h1>{{ y }}</h1>
  </div>
</template>

<script>
import { ref, onMounted, getCurrentInstance } from "vue";

export default {
  data() {
    return {
      x: this.$route.query.x
    }
  },

  setup() {
    let y = ref('');

    onMounted(() => {
      const instance = getCurrentInstance();
      y.value = instance.proxy.$route.query.y;
    });

    return {
      y
    };
  }
}
</script>