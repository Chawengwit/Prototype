<template>
  <div id="ContentZone">
    <div class="content">
      <router-view></router-view>
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scopted>
    .content{
        padding: 40px;

        display: flex;
        justify-content: center;
        align-items: center;

        border-radius: 10px;
        border: 1px solid salmon;
    }
</style>