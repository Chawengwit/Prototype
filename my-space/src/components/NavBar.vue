<template>
    <div id="navBar">
        <ul>
            <li><router-link to="/">Home</router-link></li>
            <li><router-link to="/gallery">Gallery</router-link></li>
            <li><router-link to="/about">About</router-link></li>
            <li><router-link to="/contact">Contact</router-link></li>
        </ul>
    </div>
</template>

<script>
export default {
    name: "navBar"

}
</script>

<style scoped>
    ul{
        padding: 20px;
        background-color: whitesmoke;
        text-align: center;
    }
    li{
        display: inline;
        margin-right: 20px;
    }
    a{
        font-size: 20px;
        font-weight: bold;
        color: saddlebrown;
        text-decoration: none;
    }
    a:hover {
        color: brown;
    }
</style>