<template>
    <b-form>
        <b-input-group>
            <b-form-input placeholder="Filter..." v-model="keyword"/>
            <b-form-select slot="append" v-model="selected" :options="filters" />
        </b-input-group>
    </b-form>
</template>

<script>
export default {
    name: 'FilterBar',
    data: function() {
        return {
            keyword: '',
            selected: 'title',
            filters: {
                title: 'By Title',
                author: 'By Author'
            }
        }
    }
}
</script>

<style scoped>

</style>
