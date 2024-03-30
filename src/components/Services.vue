<template>
    <div class="services">
        <div class="services-header">
            <h2>Our Services</h2>
            <p>Your Reliable Partner for Transportation in Jaipur</p>
        </div>
        <div class="services-content">
            <div class="service">
                <img src="/airport.jpeg" alt="Taxi Services">
                <h3>Airport Transfers</h3>
                <p>Need a ride to or from the airport? We offer reliable airport transfer services to make your travel
                    experience hassle-free. Our drivers will pick you up or drop you off at the airport on time, so you
                    can focus on your journey.</p>
            </div>
            <div class="service">
                <img src="/citytours.jpeg" alt="Taxi Services">
                <h3>City Tours</h3>
                <p>Explore the Pink City with our city tour packages. We offer a range of tours that cover all the major
                    attractions in Jaipur, including the Amer Fort, City Palace, Hawa Mahal, and more.</p>
            </div>
            <div class="service">
                <img src="/statetours.jpeg" alt="Taxi Services">
                <h3>Outstation Trips</h3>
                <p>Planning a trip outside Jaipur? We provide outstation taxi services to all major destinations in
                    Rajasthan and beyond. Our fleet of vehicles is well-maintained and driven by experienced drivers to
                    ensure a safe and comfortable journey.</p>
            </div>

        </div>
    </div>

</template>

<script setup>
</script>

<style scoped>
.services {
    width: 100%;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    overflow: hidden;
    background-color: #fae4d4;
}

.services-header {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    text-align: center;
}

.services-header h2 {
    font-size: 2rem;
    margin: 0;
    color: #451d03;
}

.services-header p {
    font-size: 1.25rem;
    color: #451d03;
}



.services-content {
    display: flex;
    width: 90%;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    margin-top: 2rem;
}

@media (min-width: 768px) {



    .service {
        width: 25vw;
        height: 60vh;
        position: relative;
        overflow: hidden;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding: 2rem;
        background-color: #000;
    }

    .service img {
        position: absolute;
        width: 25vw;
        height: 60vh;
        object-fit: cover;
        z-index: 0;
        left: 0;
        top: 0;
        background: #000;
        opacity: 0.7;
    }

    .service h3 {
        position: relative;
        z-index: 1;
        font-size: 2rem;
        color: #fff;
        margin-bottom: 1rem;
        transition: 0.5s ease-in-out;
        transform: translateY(100px);
    }

    .service:hover h3 {
        transition: 0.5s ease-in-out;
        transform: translateY(0px);
    }

    .service p {
        height: 40%;
        opacity: 0;
        position: relative;
        z-index: 1;
        font-size: 1rem;
        color: #fff;
        margin-bottom: 1rem;
        text-align: center;
        transition: 1s ease-in-out;
        transform: translateY(100px);
    }

    .service:hover p {
        opacity: 1;
        transform: translateY(0px);
        transition: 0.5s ease-in-out;

    }

}

@media (max-width: 768px) {

    .services-header h2 {
        font-size: 2rem;
        color: #451d03;
        margin-top: 5vh;
    }

    .services-header p {
        font-size: 0.75rem;
        color: #451d03;
    }

    .services-content {
        display: flex;
        width: 90%;
        flex-direction: column;
        align-items: center;
        flex-wrap: wrap;
        margin-top: 2rem;
    }

    .service {
        width: 70vw;
        height: 40vh;
        position: relative;
        overflow: hidden;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding: 2rem;
        background-color: #000;
        margin-bottom: 5%;
    }

    .service h3 {
        z-index: 1;
        font-size: 1rem;
        color: #fff;
        margin-bottom: 1rem;
    }

    .service p {
        opacity: 1;
        z-index: 1;
        font-size: 0.75rem;
        color: #fff;
        margin-bottom: 1rem;
        text-align: center;
    }

    .service img {
        position: absolute;
        width: 100%;
        height: 100%;
        object-fit: cover;
        z-index: 0;
        left: 0;
        top: 0;
        background: #000;
        opacity: 0.7;
    }

}
</style>