<template>
  <header class="header">
    <h1>TodoList</h1>
    <div id="nav">
      <!-- Similar to 'a' & 'href' -->
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
  </header>
</template>


<script>
export default {
  name: "Header",
};
</script>


<style scoped>
.header {
  text-align: center;
  padding: 10px;
}
</style>