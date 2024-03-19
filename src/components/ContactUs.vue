<template>
    <div class="contact">
        
        <div class="form">
            <h1>Contact Us</h1>
            <p>Feel free to contact us for any queries or feedback.</p>
            <form @submit="submitForm">
                <div>
                    <label for="name">Name:</label>
                    <input type="text" id="name" placeholder="Name" v-model="name" required>
                </div>
                <div>
                    <label for="email">Email:</label>
                    <input type="email" id="email" placeholder="Email" v-model="email" required>
                </div>
                <div>
                    <label for="message">Message:</label>
                    <textarea id="message" placeholder="Message" v-model="message" required></textarea>
                </div>
                <button type="submit">Submit</button>
            </form>
        </div>
        <div class="imgdiv">
            <img src="/contactus.jpeg" alt="about" class="bgimg"/>
            <p>" Jaisalmer fort "</p>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            name: '',
            email: '',
            message: ''
        };
    },
    methods: {
        submitForm() {
            console.log('Form submitted!');
            console.log('Name:', this.name);
            console.log('Email:', this.email);
            console.log('Message:', this.message);
        }
    }
};
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
        background-color:#fae4d4 ;
    }

    .content {
        width: 40%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        z-index: 2;
    }

    .form {
        width: 40%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        z-index: 2;
    }

    .form h1{
        color: #451d03;
        font-size: 3rem;
    }

    .form p{
        color: #451d03;
        font-size: 1.5rem;
        line-height: 1rem;
    }

    form {
        width:100%;
        margin-top: 2rem;
    }

    form div {
        margin: 1rem 0;
        width: 100%;
        display: flex;
        flex-direction: column;
        align-items: flex-start;
    }

    form input { 
        width: 100%;
        padding: 0.5rem;
        color: black;
    }

    form label {
        color: #451d03;
    }

    form textarea { 
        width: 100%;
        padding: 0.5rem;
        height: 10vh;
        color: black;
    }

    form button { 
        padding: 0.75rem 2rem;
        margin-top: 1rem;
        border: none;
        background-color: #451d03;
        color: white;
        font-size: 1rem;
        cursor: pointer;
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

.bgimg {
    width: 30vw;
    height: 70vh;
    object-fit: cover;
    left: 0;
    background-color: black;
    z-index: 0;
}
    
</style>