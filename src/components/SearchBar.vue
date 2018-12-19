<template>
    <b-nav-form>
        <b-form-input class="mr-sm-2" type="text" placeholder="Search"></b-form-input>
        <b-button variant="secondary" type="submit">Search</b-button>
    </b-nav-form>
</template>

<script>
import bNavForm from 'bootstrap-vue/es/components/nav/nav-form'
import bFormInput from 'bootstrap-vue/es/components/form-input/form-input'
import bButton from 'bootstrap-vue/es/components/button/button'

export default {
    name: 'SearchBar',
    components: {
        bNavForm,
        bFormInput,
        bButton
    }
}
</script>

<style scoped>

</style>


