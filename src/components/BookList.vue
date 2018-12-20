<template>
    <b-list-group>
        <b-list-group-item v-for="book in books" v-bind:key="book.id">
            <b-row>
                <b-col cols="9">
                    <b-row>{{ book.title }}</b-row>
                    <b-row>Author: {{ book.author }}</b-row>
                </b-col>
                <b-col>
                    <b-button>Add To Cart</b-button>
                </b-col>
            </b-row>
        </b-list-group-item>
    </b-list-group>
</template>

<script>
export default {
    name: 'BookList',
    props: ['books']
}
</script>

<style scoped>

</style>


