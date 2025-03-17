<template>
    <h1>Hello Component</h1>
    <p>{{ name }}</p>
    <p>{{ email }}</p>
</template>

<script>
export default {
    name: 'HeaderTest',
    props: {
        // 定義型別
        name: String,
        email: {
            type: String,
            default: 'demo@demo'
        }
    },
};
</script>

<style></style>