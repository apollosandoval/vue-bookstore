<template>
    <b-navbar type="dark" variant="primary">
        <b-navbar-brand>Vue Bookstore</b-navbar-brand>
        <SearchBar />
    </b-navbar>
</template>

<script>
import bNavbar from 'bootstrap-vue/es/components/navbar/navbar'
import bNavbarBrand from 'bootstrap-vue/es/components/navbar/navbar-brand'
import SearchBar from './SearchBar'
// What is a plug-in? When Do I use one?

export default {
    name: 'TopNav',
    components: {
        bNavbar,
        bNavbarBrand,
        SearchBar
    }
}
</script>

<style scoped>

</style>
