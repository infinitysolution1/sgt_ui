<template>
    <div class="container">
        <h1>Shree Govind Tourism</h1>
        <div class="footer">
            <div class="section info">
                <h3>Contact</h3>
                <p>+91 7976711820 , +91 9829285925</p>
                <h3>Address</h3>
                <p>32/406, Sector 3, near KV-6 Basketball Court, Sanganer, Sector 3, Pratap Nagar, Jaipur, Rajasthan
                    302033</p>
            </div>
            <div class="section map">
                <iframe
                    src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d113954.10540303911!2d75.6512787972656!3d26.80603360000001!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x396dcb08b5e87831%3A0x53dfe8db4b684dee!2sShree%20Govind%20Tourism!5e0!3m2!1sen!2sin!4v1710845120452!5m2!1sen!2sin"
                    width="100%" height="250" style="border:0;" allowfullscreen="" loading="lazy"
                    referrerpolicy="no-referrer-when-downgrade"></iframe>
            </div>
            <div class="section">
                <h3>Office Hours</h3>
                <p>Monday - Friday: 9am - 5pm</p>
            </div>
            <div class="section">
                <h3>Links</h3>
                <ul>
                    <li><a v-on:click="scroll">Home</a></li>
                    <li><a v-on:click="about">About</a></li>
                    <li><a v-on:click="services">Services</a></li>
                    <li><a v-on:click="contact">Contact Us</a></li>
                </ul>
            </div>

        </div>
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
</script>

<style scoped>
.container {
    width: 100%;
    display: flex;
    flex-direction: column;
    overflow-y: hidden;
    z-index: 0;
    background-color: #451d03;
    padding: 20px;
}

.container h1 {
    color: #fff;
    font-size: 2rem;
    margin-bottom: 20px;
}

.footer {
    text-align: center;
    display: flex;
    flex-direction: row;
    width: 100%;
    justify-content: space-between;

}

.section {
    width: 10vw;
    color: #fff;
}

.info {
    width: 20vw;
}

.map {
    width: 30vw;
}

h3 {
    font-size: 24px;
    color: #fff;
    text-align: left;
}

p {
    font-size: 16px;
    color: #fff;
    text-align: left;
    margin-bottom: 20px;
}

ul {
    list-style: none;
    padding: 0;
    margin: 0;
    color: #fff;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    margin-top: 8px;
}

li {
    display: inline-block;
    color: #fff;
}

a {
    color: #fff;
    font-size: 16px;
    text-decoration: none;
}

a:hover {
    text-decoration: underline;
    background-color: transparent;
}

@media (max-width: 768px) {

    .footer {
        text-align: center;
        display: flex;
        flex-direction: column;
        width: 100%;
        justify-content: space-between;

    }

    .section {
        width: 90%;
        color: #fff;
    }

    .info {
        width: 90%;
        margin-top: 2.5%;
    }

    .section {
        width: 90%vw;
        color: #fff;
        margin-top: 2.5%;
    }

    .map {
        width: 90%;
    }

}
</style>