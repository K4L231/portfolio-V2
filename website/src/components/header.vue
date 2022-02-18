<script lang="ts">
export default {
    name: 'header',
    methods: {
        show: function show(){
            alert('d')
        }
    }
}


</script>

<template>
    <div class="header">
        <div class="title">
            <span class="logo">
                <img src="./icons/logo.png" alt="">
            </span>
            <a href="" class="name">Matas</a>
        </div>

        <div class="nav">
            
            <button class="link" @click="show">Home</button>
            <button class="link">Contacts</button>
            <button class="link" >GitHub</button>
        </div>
    </div>


</template>

<style scoped>
    * {
        font-family: -apple-system,system-ui,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,sans-serif;
    }
    a{
        text-decoration: none;
    }
    .header {
        width: 100%;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
    }
    .title {
        display: flex;
        align-self: center;
    }
    .logo {
        height: 64px;
        width: 64px;
        margin-right: 10px; 
    }
    .logo img {
        height: 100%;
    }
    .title .name {
        color: #1A202C;
        font-size: 20px;
        font-weight: 700;
        letter-spacing: 0px;
        align-self: center;
    }
    .nav {
        height: 100%;
        display: flex;
        align-self: center;
    }
    .nav .link {

        font-size: 16px;
        font-weight: 600;
        color: #2D3748;
        height: 40px;
        padding-left: 20px;
        padding-right: 20px;

        border-radius: 7px;
        border: none;

        background-color: #F3F3F3;
        

    }

    .nav .link:hover {
        background-color: #aa8ed62d;
    }
    


</style>