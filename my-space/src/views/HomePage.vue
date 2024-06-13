<template>
    <div id="homePage">
        <h1>Home Page</h1>
        <input v-model="message" type="text" placeholder="Enter your message.">
        <div>{{ message }}</div>
        <button @click="message = ''">Reset</button>

    </div>
</template>

<script>
export default {
    name: "homePage",
    data() {
        return {
            message: ""
        }
    },
};
</script>

<style>

</style>