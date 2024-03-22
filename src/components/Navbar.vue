<template>
    <div :class="{ 'navbar': true, 'scrolled': scrollHeight > 40 }">
        <h1>Shree Govind Tourism</h1>
        <ul>
            <li><a v-on:click="scroll">Home</a></li>
            <li><a v-on:click="about">About</a></li>
            <li><a v-on:click="services">Services</a></li>
            <li><a v-on:click="contact">Contact Us</a></li>
        </ul>
    </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';

const scrollHeight = ref(0);

const scroll = () => {
    const homeElement = document.getElementById('home');
    if (homeElement) {
        homeElement.scrollIntoView({ behavior: 'smooth', block: 'start' });
    }
};

const about = () => {
    const aboutElement = document.getElementById('about');
    if (aboutElement) {
        aboutElement.scrollIntoView({ behavior: 'smooth', block: 'start' });
    }
};

const services = () => {
    const servicesElement = document.getElementById('services');
    if (servicesElement) {
        servicesElement.scrollIntoView({ behavior: 'smooth', block: 'start' });
    }
};

const contact = () => {
    const contactElement = document.getElementById('contact');
    if (contactElement) {
        contactElement.scrollIntoView({ behavior: 'smooth', block: 'start' });
    }
};

onMounted(() => {
    window.addEventListener('scroll', () => {
        scrollHeight.value = window.scrollY;
    });
});
</script>

<style scoped>
.navbar {
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: baseline;
    padding: 1.5rem 4rem;
    background-color: transparent;
    transition: background-color 1s;
}

.scrolled {
    background-color: #00000099;
    transition: background-color 1s;
}

.navbar h1 {
    font-size: 2.5rem;
    color: #fff;
}







.navbar ul {
    display: flex;
    list-style: none;
    width: 40%;
    justify-content: space-between;
}

@media (max-width: 768px) {
    .navbar ul {
        display: none;
    }

    .navbar h1 {
        width: 100%;
        text-align: center;
        font-size: 1.25rem;
        color: #fff;
    }
}

.navbar li {
    font-size: 1.5rem;
}

.navbar a {
    text-decoration: none;
    color: white;
}

.navbar a:hover {
    background: transparent;
    color: #ffffff99;
}

.navbar p {
    font-size: 1rem;
    color: #fff;
}
</style>