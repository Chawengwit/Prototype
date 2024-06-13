<template>
  <div id="galleryPage">
    <h1>Gallery Page</h1>
    <button @click="clickMe">Hi</button>
    <button @click="clickMe2('Welcome')">Hey</button>
    <h3>{{ getTimestamp() }}</h3>
  </div>
</template>

<script>
export default {
    name: "galleryPage",

    mounted() {
      this.initial();
    },

    methods: {
      initial(){
        console.log('ready');
      },
      clickMe(){
        alert('Hii i i');
      },
      clickMe2(msg) {
        alert(msg);
      },
      getTimestamp() {
        return Date();
      }
    },
    
}
</script>

<style>

</style>