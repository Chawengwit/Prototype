<template>
  <div id="galleryPage">
    <h1>Gallery Page</h1>
    <div>
      <img v-for="(image, index) in images" :key="index" v-bind:src="image">
    </div>
    <div>
      <p :class="[colorClass[0], colorClass[1]]"> Lorem ipsum dolor sit, amet consectetur adipisicing elit. Vitae, fugit. </p>
      <p :style="{color :  styleBind['color'], fontSize : styleBind['fontSize']}"> Lorem ipsum dolor sit, amet consectetur adipisicing elit. Vitae, fugit. </p>
      <p :style="styleBind"> Lorem ipsum dolor sit, amet consectetur adipisicing elit. Vitae, fugit. </p>
    </div>
  </div>
</template>

<script>
export default {
    name: "galleryPage",
    data() {
      return {
        images : [ "https://plus.unsplash.com/premium_photo-1674676471322-ee4276f27e34?q=80&w=1978&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D", "https://images.unsplash.com/photo-1717738118267-99f7c371127c?q=80&w=1974&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D", "https://images.unsplash.com/photo-1718033938129-842b8abdc949?q=80&w=1974&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D" ],
        colorClass : [ "textSalmon", "font20"],
        styleBind : {
          color : "blueviolet",
          fontSize: "25px",
          backgroundColor : "antiquewhite"
        }
      }
    },
}
</script>

<style scoped>
  img {
    height: 100px;
    margin-right: 20px;
  }

  .textSalmon {
    color: salmon;
  }

  .font20{
    font-size: 20px;
  }

</style>