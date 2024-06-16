<template>
    <div id="homePage">
        <h1>Home Page</h1>

        <h2 v-if="haveMessage  && count>10"> Wow your have 2 action </h2>

        <br><br>

        <span>
            <div>This message : {{ message }}</div>
            <div>Have message : {{ haveMessage }}</div>
            <input v-model="message" @change="checkMessage(message)" type="text" placeholder="Enter your message.">
            <button @click="message = '', haveMessage = false">Reset message</button>
        </span>

        <br><br>

        <span>
            <h2 v-if="count > 10">Count more than 10!!</h2>
            <button @click="count++">Count</button>
            <button @click="count=0">Reset count</button>
            <span>{{ count }}</span>
        </span>

    </div>
</template>

<script>
export default {
    name: "homePage",
    methods: {
        checkMessage(message){
            return this.haveMessage = message != "" ? true : false ;
        }
    },
    mounted() {
        this.message = "",
        this.haveMessage = false;
    },
    data() {
        return {
            message: "",
            count: 0,
            haveMessage: false,
        }
    },
};
</script>

<style>

</style>