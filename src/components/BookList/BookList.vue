<template>
  <table>
    <BookListItem
      v-for="(book, index) in books"
      :key="book.isbn"
      v-bind="book"
      @read="readBook(index)"
    />
  </table>
</template>

<script>
import BookListItem from "@/components/BookListItem/BookListItem.vue";

import BOOKS from "./books";

export default {
  name: "BookList",
  components: {
    BookListItem,
  },
  data() {
    return {
      books: [],
    };
  },
  methods: {
    readBook(index) {
      this.books[index] = {
        ...this.books[index],
        read: true,
      };
    },
  },
  created() {
    this.books = [...BOOKS];
  },
};
</script>

<style lang="scss">
$grey-color: #dddddd;

table {
  font-family: "Trebuchet MS", Arial, Helvetica, sans-serif;
  border-collapse: collapse;
  width: 100%;

  td,
  th {
    border: 1px solid $grey-color;
    padding: 8px;
  }

  th {
    padding-top: 12px;
    padding-bottom: 12px;
    text-align: left;
    background-color: #4caf50;
    color: white;
  }

  tr:nth-child(even) {
    background-color: #f2f2f2;
  }

  tr:hover {
    background-color: $grey-color;
  }
}
</style>
