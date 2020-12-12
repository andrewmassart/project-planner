<template>
  <nav class="main-nav">
    <router-link :to="{ name: 'Home' }">Projects</router-link>
    <router-link :to="{ name: 'AddProject' }">Add new project</router-link>
  </nav>
</template>

<script>
export default {};
</script>

<style>
.main-nav {
  text-align: center;
  margin: 40px auto;
}
.main-nav a{
    display: inline-block;
    text-decoration: none;
    margin: 0 10px;
    color: #999;
    font-size: 18px;
}
.main-nav a:hover {
    color: #555;
    transition: .2s ease-in-out;

}
a.router-link-active {
    border-bottom: 2px solid #555;
    color: #555;
    font-weight: bold;
    padding-bottom: 4px;
}
</style>