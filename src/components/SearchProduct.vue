<script>
export default {
    name: 'SearchProduct',
    data: () => ({
        product: ''
    }),
    props: {
        buttonText: String,
        placeholder: String,
    },
    emits: ['form-submit']
}
</script>

<template>
    <form @submit.prevent="$emit('form-submit', product)">
        <input type="text" :placeholder="placeholder" v-model.trim="product">
        <button>{{ buttonText }}</button>
    </form>
</template>

<style></style>