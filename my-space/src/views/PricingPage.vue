<template>
    <div id="pricingPage">

        <ClockTime> 
            <template v-slot:slot_name_1>
                <span>{{ time_en }}</span>
            </template>
        </ClockTime>

        <ClockTime> 
            <template v-slot:slot_name_2>
                <span>{{ time_th }}</span>
            </template>
        </ClockTime>
    </div>
</template>

<script>
import ClockTime from '@/components/ClockTime.vue';

export default {
    name: "pricingPage",
    data() {
        return {
            time_en : "Time now : ",
            time_th : "เวลาตอนนี้ : "
        }
    },
    components:{
        ClockTime,
    }
}
</script>

<style>

</style>