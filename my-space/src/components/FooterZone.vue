<template>
  <div id="footerZone">
    <footer>
      <span>{{ text }}</span>
    </footer>
  </div>
</template>

<script>
export default {
  name: "footerZone",
  mounted() {
    setInterval(()=>{
      this.$emit("onTime", Date());
    }, 100);
  },
  props:[
    "text",
  ]
}
</script>

<style scoped>
  footer{
    width: 100%;
    position: absolute;
    bottom: 0;
    
    display: flex;
    justify-content: center;
    align-items: center;

    background-color: whitesmoke;

    padding: 20px;
  }

  span{
    color: saddlebrown;
    font-size: 20px;
    font-weight: bold;
  }
</style>