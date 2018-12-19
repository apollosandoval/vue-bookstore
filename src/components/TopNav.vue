<template>
    <b-navbar type="dark" variant="primary">
        <b-navbar-brand>Vue Bookstore</b-navbar-brand>
        <SearchBar />
    </b-navbar>
</template>

<script>
// import { Navbar } from 'bootstrap-vue/es/components' 
import SearchBar from './SearchBar'
// What is a plug-in? When Do I use one?

export default {
    name: 'TopNav',
    components: {
        SearchBar
    }
}
</script>

<style scoped>

</style>
