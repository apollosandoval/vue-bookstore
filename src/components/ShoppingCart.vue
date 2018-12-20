<template>
    <b-list-group>
        <b-list-group-item>Total: </b-list-group-item>
        <b-list-group-item v-for="book in booksInCart" v-bind:key="book.id">{{book.title}}</b-list-group-item>
    </b-list-group>
</template>

<script>
export default {
    name: 'ShoppingCart',
    props: ['booksInCart']
}
</script>

<style scoped>

</style>

