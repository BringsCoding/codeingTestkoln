<template>
  <ul>
    <li><a class="active" href="#books">Books</a></li>
    <li><a href="#about">About</a></li>
  </ul>
</template>

<style lang="scss">
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: hidden;
  background-color: #333333;

  li {
    float: left;
  }

  a {
    display: block;
    color: white;
    text-align: center;
    padding: 14px 16px;
    text-decoration: none;

    &:hover:not(.active) {
      background-color: #111111;
    }

    &.active {
      background-color: #4caf50;
    }
  }
}
</style>
