<script lang="ts">
export default {
    name: 'header',
    data: function () {
        return {
            isShow: false,
            burger: false,
            burgerExpand: false
        }
    },
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
            <div class="link" :class="{ 'border' : isShow}" ><a class="nav-text" @click="isShow = !isShow">Contacts</a>
                <div class="expanded" v-if="isShow">
                    <div class="info">
                        <h2><b>Contacts</b></h2>
                        <p>Ways to contact me</p>
                    </div>
                    <div class="info details">
                        <h2>📧 Gmail</h2>
                        <p>matasalzo@gmail.com</p>
                    </div>
                    <div class="info details">
                        <h2>💣 Discord</h2>
                        <p>K4L#0415</p>
                    </div>
                </div>
                
            </div>
            <div class="link"><a href="" class="nav-text">Home</a></div>
            <div class="link" ><a href="https://github.com/K4L231" target="_blank" class="nav-text">GitHub</a></div>
        </div>
        <div class="hamburger" @click="burger = !burger">
            <span class="burger">☰</span>
        </div>
    </div>


    <div class="hamburger-menu" v-if="burger">
        <a href="" class="burger-link">Home</a>
        <a href="https://github.com/K4L231" target="_blank" class="burger-link" >GitHub</a>
        <a class="burger-link" @click="burgerExpand = !burgerExpand">
            Contacts<img :class="{ 'arrow' : burgerExpand }" class="expand-arrow" src="https://img.icons8.com/ios/16/000000/expand-arrow--v3.png"/></a>
                <div v-if="burgerExpand">
                    <div class="info burger-expand">
                        <h2><b>Contacts</b></h2>
                        <p>Ways to contact me</p>
                    </div>
                    <div class="info details burger-expand">
                        <h2>📧 Gmail</h2>
                        <p>matasalzo@gmail.com</p>
                    </div>
                    <div class="info details burger-expand">
                        <h2>💣 Discord</h2>
                        <p>K4L#0415</p>
                    </div>
                </div>
        
    </div>
</template>

<style scoped>

    a{
        text-decoration: none;
    }
    .header {
        margin-top: 20px;
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

        -webkit-user-select: none; /* Safari */        
        -moz-user-select: none; /* Firefox */
        -ms-user-select: none; /* IE10+/Edge */
        user-select: none; /* Standard */
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

        border-radius: 7px;
        border: none;

        background-color: #F3F3F3;

        display: flex;
        position: relative;

        border: 3px solid transparent;

    }

    .link .expanded {
        background-color: #FFFFFF;
        width: 350px;
        position: absolute;
        top: 50px;
        padding-top: 5px;
        padding-bottom: 5px;
        border-radius: 5px;
        left: 0px;
        cursor: default;
    }

    .nav .link:hover {
        background-color: #aa8ed62d;
        cursor: pointer;
    }
    .nav-text {
        -webkit-user-select: none; /* Safari */        
        -moz-user-select: none; /* Firefox */
        -ms-user-select: none; /* IE10+/Edge */
        user-select: none; /* Standard */
        line-height: 40px;
        width: 100%;
        text-align: center;
        color: #2D3748;

        padding-left: 20px;
        padding-right: 20px;

    }
    .info {
        padding-left: 20px;
        padding-right: 20px;
        
        padding-top: 10px;

        border-bottom: 1px solid #a0c5e869;

    }
    .info h2{
        font-size: 16px;
        margin: 0px;
    }
    .info p {
        font-size: 12px;
        color: #4A5568;
        margin-top: 0px;
        margin-bottom: 10px;
    }
    .info.details {
        border: none;
        padding-top: 10px;
    }
    .info.details h2{
        font-size: 14px;
    }
    .info.details p{
        font-size: 14px;
        margin-bottom: 0px;
    }
    .link.border {
        border: 3px solid #AA8ED6;
        background-color: #aa8ed62d;
    }
    .burger {
        margin: auto;
        font-size: 27px;
        font-weight: 900;
        display: none;
    }
    .hamburger {
        align-self: center;
        display: none;
    }
    .hamburger:hover {
        cursor: pointer;
        -webkit-user-select: none; /* Safari */        
        -moz-user-select: none; /* Firefox */
        -ms-user-select: none; /* IE10+/Edge */
        user-select: none; /* Standard */
    }
    .hamburger-menu {
        position: absolute;
        width: 250px;
        background-color: #ffffff;
        right: 0px;
        display: none;
        flex-direction: column;
        
        padding-right: 20px;
        
        padding-top: 5px;
        padding-bottom: 10px;

        border-top-left-radius: 10px;
        border-bottom-left-radius: 10px;
    }
    .burger-link {
        color: #2D3748;

        font-size: 16px;
        font-weight: 600;

        padding-left: 20px;
        width: 100%;

        padding-top: 15px;
        padding-bottom: 15px;

        margin-top: 5px;
        margin-bottom: 5px;

    }
    .burger-link a {
        display: flex;
        flex-direction: row;
    }

    .info.burger-expand {
        margin-left: 15px;
        background-color: #FFFFFF;
    }
    .burger-link:hover {
        background-color: #aa8ed62d;
        cursor: pointer;
    }
    .arrow {
        
        -webkit-transform:rotate(270deg);
        -moz-transform: rotate(270deg);
        -ms-transform: rotate(270deg);
        -o-transform: rotate(270deg);
        transform: rotate(270deg);
    }
    .expand-arrow {
        height: 14px;
        margin-left: 15px;

    }

    @media (max-width: 650px) {
        .burger {
        display: flex;
        }
        .hamburger {
            display: flex;
        }
        .hamburger-menu {
            display: flex;
        }
        .nav {
            display: none;
        }
    }

</style>