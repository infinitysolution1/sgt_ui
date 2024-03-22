<template lang="">
  <div class="home" id="home">
    <img src="/homebg.jpeg" alt="home" class="bgimg" />
    <div class="content">
      <p>Welcome to</p>
      <h1>Shree Govind Tourism</h1>
      <button v-on:click="scroll">Book Now</button>
      <div class="or">
        <span></span>
        <p>Or</p>
        <span></span>
      </div>
      <div class="call">
      <h2>Contact us on </h2>
      <p>+91 7976711820, +91 9829285925</p>
    </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const scroll = () => {
    window.scrollTo({
        top: document.documentElement.scrollHeight,
        behavior: "smooth"
    });
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

.or {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    margin-top: 2.5%;
}

.or span {
    width: 10vw;
    border-bottom: 2px solid white;
    margin: 0 1rem;
}

.call {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-top: 2.5%;
    width: 50%;

}

.call p {
    z-index: 2;
    font-size: 1.5rem;
    color: white;
    font-weight: bold;
    padding: 0% 2.5%;
    background-color: #00000077;
}

.call h2 {
    z-index: 2;
    font-size: 1.5rem;
    color: white;
    font-weight: bold;
}



@media (max-width: 768px) {
    .content h1 {
        font-size: 2rem;
        color: white;
        line-height: 8rem;
        text-align: center;
    }

    .content p {
        font-size: 1rem;
        color: white;
    }

    .or span {
        width: 30vw;
        border-bottom: 2px solid white;
        margin: 0 1rem;
    }

    .call {
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        margin-top: 2.5%;
        width: 90%;

    }
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
