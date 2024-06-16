<template>
  <div id="aboutPage">
    <h1>About Page</h1>

    <div>
      <div>Your fullname : {{ renderFullname }}</div>
      <div>Your nickname : {{ userInfo['nickname'] }}</div>
      <ul>
        <li v-for="(item, index) in colors" :key="index">color : {{ item }}</li>
      </ul>

    </div>
    
  </div>
</template>

<script>
export default {
    name: "aboutPage",
    data() {
      return {
        userInfo: {
          "firstname" : "Chawengwit",
          "lastname" : "Wongviriyasakul",
          "nickname" : "Hog",
        },
        colors : ["red", "yellow", "green"]
      }
    },
    computed: {
      renderFullname(){
        return this.userInfo['firstname'] + " " + this.userInfo['lastname'];
      }
    }
}
</script>

<style>

</style>