<template>
  <AppNavigation />
  <BookList />
</template>

<script>
import AppNavigation from "./components/AppNavigation/AppNavigation.vue";
import BookList from "./components/BookList/BookList.vue";

export default {
  name: "App",
  components: {
    AppNavigation,
    BookList,
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
