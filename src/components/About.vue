<template>
    <div class="about">
        <div class="imgdiv">
            <img src="/bg.jpeg" alt="about" class="bgimg" />
            <p>" Toorji Ka Jhalra Bavdi "</p>
            <h3>Jodhpur</h3>
        </div>
        <div class="content">
            <h2>About Us</h2>
            <p>Shree Govind Tourism is a leading taxi service provider in Jaipur, dedicated to delivering exceptional
                transportation solutions to our customers. With years of experience in the industry, we have established
                ourselves as a trusted name known for reliability, punctuality, and customer satisfaction.</p>
            <p>Our mission is to provide safe, convenient, and affordable transportation services that exceed our
                customers' expectations. Whether you need a ride to the airport, a city tour, or an outstation trip, you
                can rely on us to get you to your destination comfortably and on time.</p>
        </div>
    </div>
</template>

<style scoped>
.about {
    width: 100%;
    height: 100vh;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    overflow: hidden;
    padding: 5rem 5rem;
    background-color: #fae4d4;
}

.content {
    width: 60%;
    display: flex;
    flex-direction: column;
    z-index: 2;
    color: #451d03;
}

.content h2 {
    font-size: 3rem;
    text-align: start;
}

.content p {
    font-size: 1.5rem;
    text-align: start;
    margin-top: 2rem;
}

.imgdiv {
    display: flex;
    flex-direction: column;
}

.imgdiv p {
    font-size: 1rem;
    color: #451d03;
    text-align: center;
    z-index: 2;
    margin-top: 1rem;
    font-style: italic;
}

.imgdiv h3 {
    font-size: 1rem;
    color: #451d03;
    text-align: center;
}

.bgimg {
    width: 30vw;
    height: 70vh;
    object-fit: cover;
    left: 0;
    background-color: black;
    z-index: 0;
}

@media (max-width: 768px) {

    .about {
        flex-direction: column-reverse;
        width: 100%;
        height: 100vh;
        display: flex;
        justify-content: space-around;
        align-items: center;
        padding: 1rem 1rem;
    }

    .content {
        width: 100%;
        display: flex;
        flex-direction: column;
        z-index: 2;
        color: #451d03;

    }

    .content h2 {
        font-size: 2rem;
        text-align: center;
    }

    .content p {
        font-size: 0.75rem;
        text-align: center;
    }

    .bgimg {
        width: 100%;
        height: 30vh;
        object-fit: cover;
        left: 0;
        background-color: black;
        z-index: 0;
    }

    .imgdiv p {
        font-size: 0.75rem;
        color: #451d03;
        text-align: center;
        z-index: 2;
        margin-top: 1rem;
        font-style: italic;
    }

    .imgdiv h3 {
        font-size: 0.75rem;
        color: #451d03;
        text-align: center;
    }
}
</style>