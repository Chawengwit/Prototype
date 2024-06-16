<template>
  <div id="clockTime">

    <slot name="slot_name_1"></slot>
    <slot name="slot_name_2"></slot>
    {{ time }}
    
  </div>
</template>

<script>
import moment from 'moment';

export default {
    name: "clockTime",
    mounted() {
        setInterval(()=>{
            this.time = moment(Date()).format("MM/DD/YYYY hh:mm:ss");
        }, 1000);
    },
    data() {
        return {
            time: ""
        }
    },


}
</script>

<style>

</style>