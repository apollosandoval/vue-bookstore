<template>
  <div id="app">
    <top-nav />
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
              <filter-bar />
            </b-col>
          </b-row>
          <b-row>
            <b-col>
              <!-- Insert BookList Component -->
              <book-list v-bind:books="books"/>
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
              <shopping-cart v-bind:booksInCart="booksInCart" />
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

import axios from 'axios'

export default {
  name: 'app',
  components: {
    'top-nav': TopNav,
    'shopping-cart': ShoppingCart,
    'book-list': BookList,
    'filter-bar': FilterBar
  },
  data() {
    return {
      books: []
    }
  },
  mounted() {
    axios
      .get('http://localhost:8082/api/books')
      .then( res => this.books=res.data )
  },
  methods: {

  },
  computed: {
    booksInCart: function() {
      return this.books.filter(book => book.inCart)
    }
  }
}
</script>

<style>

</style>
