<template lang="">
    <div class="home" id="home">
        <img src="/homebg.jpeg" alt="home" class="bgimg"/>
        <div class="content">
            <p>Welcome to</p>
            <h1> Shree Govind Tourism</h1>
            <button v-on:click="scroll">Explore</button>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue';

const scroll = () => {
    const homeElement = document.getElementById('contact');
    if (homeElement) {
        homeElement.scrollIntoView({ behavior: 'smooth' });
    }
};
</script>
<style scoped>
    .home {
        width: 100%;
        min-height: 100vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        overflow-y: hidden;
        z-index: 0;
        background-color: #000;
    }
    .bgimg {
        width: 100vw;
        height: 100%;
        object-fit: cover;
        left: 0;
        position: absolute;
        opacity: 0.7;
        background-color: black;
        z-index: 0;
    }

    .content {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        z-index: 2;
    }

    .content p {
        font-size: 1.5rem;
        color: white;
    }

    .content h1 {
        font-size: 6rem;
        color: white;
        line-height: 8rem;
    }

    .content button {
        padding: 1rem 3rem;
        margin-top: 2rem;
        border: none;
        background-color: white;
        color: #783302;
        font-size: 1rem;
        cursor: pointer;
    }
</style>