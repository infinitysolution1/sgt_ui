<template>
    <div class="fleet">
        <h1>Our Fleet</h1>
        <p>Discover Rajasthan's wonders with our diverse fleet of vehicles, ideal for city tours, desert adventures, and
            everything in between. Find your perfect ride today.</p>
        <div class="types">
            <ul>
                <li v-for="(section, index) in sections" :key="index" :class="{ active: selected === index }"><a
                        v-on:click="selectSection(index)">{{ section.section }}</a></li>
            </ul>
        </div>
        <div class="cars">
            <div class="car" v-for="(car, index) in sections[selected].cars" :key="index">
                <img :src="car.image" alt="car" class="carimg" />
                <p>{{ car.name }}</p>
            </div>
        </div>
    </div>
</template>
<script setup>
import { ref } from 'vue';
const selected = ref(0)
const sections = ref([
    {
        section: "SUV",
        cars: [
            {
                name: "Toyota Innova",
                image: "/innova.webp"
            },
            {
                name: "Ertiga",
                image: "/ertiga.webp"
            },
        ]
    },
    {
        section: "Sedan",
        cars: [
            {
                name: "Maruti Suzuki Dzire",
                image: "/baleno.webp"
            },
            {
                name: "Toyota Etios",
                image: "/etios.webp"
            },
        ]
    },

    {
        section: "Hatchback",
        cars: [
            {
                name: "Maruti Suzuki Baleno",
                image: "/baleno.webp"
            },
            {
                name: "Maruti Suzuki Celerio",
                image: "/celerio.webp"
            },
            {
                name: "Maruti Suzuki Alto",
                image: "/alto.webp"
            },
        ]
    },
])

function selectSection(index) {
    selected.value = index
}


</script>
<style scoped>
.fleet {
    width: 100%;
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    overflow: hidden;
    background-color: #fae4d4;
}

.fleet h1 {
    font-size: 3rem;
    color: #451d03;

}

.fleet p {
    font-size: 1.25rem;
    color: #451d03;
    text-align: center;
    width: 60%;
}

.types {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    margin-top: 3rem;
    width: 40%;
}

.types ul {
    display: flex;
    flex-direction: row;
    width: 100%;
    justify-content: space-between;
    align-items: center;
    list-style-type: none;
}

.types a {
    font-size: 1.5rem;
    color: #451d03;
    cursor: pointer;
    margin: 0%;
}

.types li.active {
    border-bottom: 2px solid #783302;
    line-height: -8px;
}

.types li a:hover {
    color: #78330299;
    background-color: transparent;
}

.cars {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
    margin-top: 2rem;
    width: 80%;
}

.car {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin: 1rem;
    padding: 1rem;
    border-radius: 8px;
    background-color: white;
    transition: 1s ease-in-out;
    transform: translateY(0px);
    overflow: hidden;
    position: relative;
}

.car::before {
    transform: translateY(-50px);
}

.car p {
    position: absolute;
    bottom: 0;
    padding: 1.5% 5%;
    width: 100%;
    text-align: start;
    font-size: 1.5rem;
    color: white;
    background-color: #00000055;
}

.carimg {
    width: 25vw;
    height: 30vh;
    object-fit: contain;
    border-radius: 8px;
}

@media (max-width: 768px) {


    .fleet p {
        font-size: 0.9rem;
        color: #451d03;
        text-align: center;
        width: 90%;
    }

    .types {
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        margin-top: 3rem;
        width: 80%;
    }

    .types ul {
        display: flex;
        flex-direction: row;
        width: 100%;
        justify-content: space-between;
        align-items: center;
        list-style-type: none;
    }

    .types a {
        font-size: 1.5rem;
        color: #451d03;
        cursor: pointer;
        margin: 0%;
    }

    .cars {
        display: flex;
        flex-direction: column;
        justify-content: space-around;
        align-items: center;
        margin-top: 2rem;
        width: 90%;
    }

    .car {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding: 1rem;
        border-radius: 8px;
        background-color: white;
        transition: 1s ease-in-out;
        overflow: hidden;
        position: relative;
    }


    .car p {
        position: absolute;
        bottom: 0;
        padding: 1.5% 5%;
        width: 100%;
        text-align: start;
        font-size: 1.5rem;
        color: white;
        background-color: #00000055;
    }

    .carimg {
        width: 40vw;
        height: 15vh;
        object-fit: contain;
        border-radius: 8px;
    }

}
</style>