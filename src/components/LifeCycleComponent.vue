<template>
    <p>Component</p>
</template>

<script>
export default {
    name: 'Component',
    beforeCreate() {
        console.log('Component beforeCreate');
    },
    created() {
        console.log('Component created');
    },
    beforeMount() {
        console.log('Component beforeMount');
    },
    mounted() {
        console.log('Component mounted');
    },
    beforeUpdate() {
        console.log('Component beforeUpdate');
    },
    updated() {
        console.log('Component updated');
    },
};
</script>