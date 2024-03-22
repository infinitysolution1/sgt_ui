<template lang="">
    <div class="testimonials">
        <img class="bg" src="/testimonials.jpeg"/>
        <h1>Testimonials</h1>
        <div class="testimonial-list">
            <div class="testimonial-items" v-for="testimonial in testimonials" :key="testimonial.author">
                <img class="quote" src="/quote.png" alt="quote" />
                <h3>{{ testimonial.author }}</h3>
                <p>{{ testimonial.testimonial }}</p>
                <img class="rating" src="/rating.webp"/>
            </div>
        </div>
    </div>
</template>
<script setup>
import { ref } from 'vue';

const testimonials = ref(
    [
        {
            "author": "Ramesh Sharma",
            "testimonial": "Booking Shree Govind Tourism for my trip in Rajasthan was the best decision I made! The drivers were punctual, the cars were clean and comfortable, and the service was impeccable. Highly recommended for anyone exploring the beauty of Rajasthan!"
        },
        {
            "author": "Priya Patel",
            "testimonial": "Shree Govind Tourism made my journey through Rajasthan truly memorable. From the moment I booked until the end of my trip, their team provided exceptional service. Courteous drivers, reliable pickups, and a smooth ride throughout. Will definitely choose them again!"
        },
        {
            "author": "Anil Singh",
            "testimonial": "I recently used Shree Govind Tourism for my family vacation in Rajasthan, and I couldn't be happier with the experience. The driver was knowledgeable about the local sights, and the car was well-maintained and comfortable. Thank you for making our trip hassle-free!"
        }
    ]
)

</script>
<style scoped>
.testimonials {
    width: 100%;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
    overflow: hidden;
    position: relative;
    background-color: #fae4d4;
}

.testimonials h1 {
    font-size: 3rem;
    color: #451d03;
}

.bg {
    width: 100%;
    height: 120vh;
    object-fit: cover;
    margin-top: 2rem;
    position: absolute;
    background-color: #fff;
    z-index: 0;
    opacity: 0.3
}

.testimonial-items {
    width: 30%;
    height: 30vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    z-index: 1;
}

.testimonial-list {
    width: 90%;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
    flex-wrap: wrap;

}

.quote {
    width: 50px;
    height: 50px;
    background-color: transparent;
    color: #451d03;
}

.testimonial-items h3 {
    font-size: 1.5rem;
    color: #451d03;
    margin-top: 1rem;
    z-index: 1;
}

.testimonial-items p {
    font-size: 1.25rem;
    color: #451d03;
    text-align: center;
    margin-top: 1rem;
}

.rating {
    height: 80px;
    scale: 1;
    background-color: transparent;
    color: #451d03;
    margin-bottom: 2.5%;
}

@media (max-width: 768px) {



    .testimonials {
        width: 100%;
        height: 100vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        overflow: hidden;
        position: relative;
        background-color: #fae4d4;
    }

    .testimonials h1 {
        font-size: 2rem;
        color: #451d03;
    }

    .testimonial-list {
        width: 90%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
    }

    .testimonial-items {
        width: 100%;
        height: 25vh;
        display: flex;
        flex-direction: column;
        padding: 0 1rem;
        z-index: 1;
        margin-top: 5%;
        position: relative;
    }

    .quote {
        width: 24px;
        height: 24px;
        background-color: transparent;
        color: #451d03;
        top: 0;
    }



    .testimonial-items h3 {
        font-size: 1rem;
        color: #451d03;
        z-index: 1;
        margin-top: 4px;
    }

    .testimonial-items p {
        font-size: 0.6rem;
        color: #451d03;
        text-align: center;
        margin-top: 4px;
    }

    .rating {
        scale: 1;
        width: 100%;
        bottom: 0;
        background-color: transparent;
        color: #451d03;
        object-fit: contain;
        margin-bottom: 0px;
        margin-top: 0px;
    }

}
</style>