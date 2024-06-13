<template>
  <div id="app">
    <ul>
      <li><router-link to="/">Home</router-link></li>
      <li><router-link to="/gallery">Gallery</router-link></li>
      <li><router-link to="/about">About</router-link></li>
    </ul>

    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: "app"
}
</script>

<style>
  ul{
    margin: 0;
    padding: 0;
  }
  li{
    display: inline;
    margin-right: 10px;
  }
</style>