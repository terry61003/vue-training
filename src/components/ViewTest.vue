<template>
    <div>
        <input type="text" v-model="text" />
        <button @click="$emit('viewText', text)">Send</button>
    </div>
</template>

<script>
export default {
    name: 'ViewTest',
    emits: ['viewText'],
    data() {
        return {
            text: '',
        };
    },
};
</script>