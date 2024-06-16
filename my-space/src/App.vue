<template>
  <div id="app">

    <NavBar/>
    <ContentZone/>
    <FooterZone text="Copyright 2024 by Chawengwit" @onTime="onTime"/>
    <span>{{ time }}</span>


  </div>
</template>

<script>
import NavBar from './components/NavBar.vue';
import ContentZone from './components/ContentZone.vue';
import FooterZone from './components/FooterZone.vue';
import moment from 'moment'

export default {
  name: "app",
  methods: {
    onTime(returnTime) {
      this.time = moment(returnTime).format("MM/DD/YYYY hh:mm:ss");
    }
  },

  data() {
    return {
      time: ""
    }
  },

  components: {
    NavBar,
    ContentZone,
    FooterZone
  }
}
</script>

<style>
  *{
    box-sizing: border-box;
  }
</style>