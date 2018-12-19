<template>
  <div id="app">
    <TopNav />
    <b-container>
      <b-row>
        <!-- BookList -->
        <b-col cols="8">
          <b-row>
            <b-col cols="6">
              <h1>List of Books</h1>
            </b-col>
            <b-col cols="6">
              <!-- Filter Input Component -->
              <FilterBar />
            </b-col>
          </b-row>
          <b-row>
            <b-col>
              <!-- Insert BookList Component -->
              <BookList />
            </b-col>
          </b-row>
        </b-col>
        <!-- Shopping Cart -->
        <b-col cols="4">
          <b-row>
            <b-col>
              <h1>Shopping Cart</h1>
            </b-col>
          </b-row>
          <b-row>
            <b-col>
              <!-- Shopping Cart Component -->
              <ShoppingCart />
            </b-col>
          </b-row>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
import TopNav from './components/TopNav'
import ShoppingCart from './components/ShoppingCart'
import BookList from './components/BookList'
import FilterBar from './components/FilterBar'

export default {
  name: 'app',
  components: {
    TopNav,
    ShoppingCart,
    BookList,
    FilterBar
  }
}
</script>

<style>

</style>
