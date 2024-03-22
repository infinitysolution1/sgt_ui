<template>
    <div class="contact">

        <div class="form">
            <iframe
                src="https://docs.google.com/forms/d/e/1FAIpQLSeFyJNrNYFmqgeXBz4N5ohpAXSlX50gN9JjZR6PJwwKf1vsZQ/viewform?embedded=true"
                class="form-iframe">Loading…</iframe>
        </div>
        <div class="imgdiv">
            <img src="/contactus.jpeg" alt="about" class="bgimg" />
            <p>" Jaisalmer fort "</p>
            <h3>Jaisalmer</h3>
        </div>
    </div>
</template>

<script setup>
</script>

<style scoped>
/* Add your custom styles here */
.contact {
    width: 100%;
    height: 100vh;
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
    overflow: hidden;
    background-color: #fae4d4;
}

.content {
    width: 20%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    z-index: 2;
}

.form {
    width: 38%;
    height: 100vh;
    display: flex;
    z-index: 2;
    border-radius: 8px;
}

.form-iframe {
    scale: 0.8;
    width: 100%;
    margin-top: -2.5%;
    background-color: white;
    border-radius: 16px;
    overflow-y: hidden;
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

    .contact {
        width: 100%;
        height: 100vh;
        display: flex;
        flex-direction: row;
        justify-content: space-around;
        align-items: center;
        overflow: hidden;
        background-color: #fae4d4;
    }

    .form {
        width: 100%;
        height: 100vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        z-index: 2;
        border-radius: 8px;
    }

    .form-iframe {
        width: 100%;
        height: 100vh;
        margin-top: -2.5%;
        background-color: white;
        border-radius: 16px;
        overflow-y: hidden;
    }

    .imgdiv {
        display: none;
    }
}
</style>