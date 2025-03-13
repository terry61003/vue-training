<template>
  <p v-if="isShow">Hello World</p>
  <p v-show="isShow">Hello World</p>
  <p v-for="(user, index) in users1" :key="user">{{ index }} {{ user }}</p>
  <p v-for="(user, index) in users2" :key="user.email">
    {{ index }} {{ user.name }} {{ user.email }}
  </p>
  <div v-for="(user, index) in users1" :key="user">
    <p v-if="user === 'Jake'">{{ index }} {{ user }}</p>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      isShow: true,
      users1: ['Jake', 'Allan', 'Eason'],
      users2: [
        { name: 'Jake', email: 'jake@gmail.com' },
        { name: 'Allan', email: 'allan@gmail.com' },
        { name: 'Eason', email: 'eason@gmail.com' },
      ],
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
