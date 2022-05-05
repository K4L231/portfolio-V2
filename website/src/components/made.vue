<template>
    <div class="main">
        <div class="intro">
            <h2 class="intro-text">Stuff I made</h2>
        </div>
        <div class="projects">

            <a href="https://github.com/K4L231/TikTok-To-Youtube-Uploads-Videos" target="_blank" class="project">
                <h2 class="project-name">🔥TikTok to Youtube</h2>
                <p class="project-about">Bot that uploads videos from TikTok to Youtube. <br> Currently it has 153 videos and 20.000+ views. <br><br>
                    <span style="color: green; margin: 0px; font-weight: 500">Click for GitHub</span>
                    <br> It is made with:
                </p>
                <ul>
                    <li>NodeJs</li>
                    <li>Puppeteer(extra stealth, adblocker)</li>
                </ul>
            </a>

            <a href="https://github.com/K4L231/TikTok-To-Youtube-Uploads-Videos" target="_blank"  class="project">
                <h2 class="project-name">🚀Crypto Dip Buying Bot</h2>
                <p class="project-about">Bot that automatically buys BTC if it falls down by 15%, once the purchase is done it notifies me on my discord channel. <br><br> 
                    <span style="color: green; margin: 0px; font-weight: 500">Click for GitHub</span>
                    <br>It is made with: 
                </p>
                <ul>
                    <li>NodeJs</li>
                    <li>Node-Binance-Api</li>
                    <li>DiscordJs</li> 
                </ul>
            </a>

            <a class="project" href="https://twitter.com/InsdrTracker" target="_blank">
                <h2 class="project-name">📈 Insider Trading Twitter Bot</h2>
                <p class="project-about">Bot goes to website, scrapes data and if its not on database, it will post on twitter
                    <span style="color: green; margin: 0px; font-weight: 500"><br><br>Click for Twitter account</span>
                    <br>It is made with:
                </p>
                <ul>
                    <li>NodeJs</li>
                    <li>Puppeteer</li>
                    <li>Twitter API</li>
                </ul>
            </a>
        </div>
        <div class="intro margin">
            <h2 class="intro-text">Websites I made</h2>
        </div>
        <div class="projects">
                        <a class="project" href="https://twitter.com/InsdrTracker" target="_blank">
                <h2 class="project-name">📈 Insider Trading Twitter Bot</h2>
                <p class="project-about">Bot goes to website, scrapes data and if its not on database, it will post on twitter
                    <span style="color: green; margin: 0px; font-weight: 500"><br><br>Click for Twitter account</span>
                    <br>It is made with:
                </p>
                <ul>
                    <li>NodeJs</li>
                    <li>Puppeteer</li>
                    <li>Twitter API</li>
                </ul>
            </a>
        </div>
    </div>
</template>

<script setup lang="ts">

</script>

<style scoped>
    .main {
        width: 100%;
    }
    .intro-text {
        font-size: 23px;
        font-weight: 700;
    }
    .projects {
        width: 100%;
        display: flex;
        flex-flow: row wrap;
        gap: 12px;
        justify-content: center;
        align-items: stretch;
        align-content: stretch;
    }
    .project {

        flex: 1 0 0px; /* or 1 0 100px, and no more need in min-width at all */
        max-width: 350px;
        min-width: 270px;


        background-color: white;
        padding-left: 12px;
        padding-right: 12px;
        padding-top: 12px;
        padding-bottom: 12px;
        border-radius: 5px;

        cursor: pointer;

        transition: transform .2s; /* Animation */

        text-decoration: none;
    }
    
    .project:hover {
        transform: scale(1.03);
    }
    .project-name {
        font-size: 16px;
        font-weight: 700;
        margin: 0px;
        margin-bottom: 5px;
        color: black;
    }
    .project-about {
        font-size: 16px;
        margin: 0px;
        color: #2D3748;
        text-decoration: none;
    }
    ul {
        color: #2D3748;
        margin-top: 5px;
        margin-bottom: 0px;
    }
    .margin {
        margin-top: 50px;
    }



    @media (max-width: 855px) {
        .main {
            margin: auto;
            margin-bottom: 20px;
            max-width: 400px;
        }
        .project {
            width: 100%;
            max-width: 400px;
            min-width: 200px;
        }
    }
</style>