<template>
    <div class="footer">
        <div class="section">
            <h3>Address</h3>
            <p>32/406, Sector 3, near KV-6 Basketball Court, Sanganer, Sector 3, Pratap Nagar, Jaipur, Rajasthan 302033</p>
        </div>
        <div class="section">
            <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d113954.10540303911!2d75.6512787972656!3d26.80603360000001!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x396dcb08b5e87831%3A0x53dfe8db4b684dee!2sShree%20Govind%20Tourism!5e0!3m2!1sen!2sin!4v1710845120452!5m2!1sen!2sin" width="100%" height="250" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
        </div>
        <div class="section">
            <h3>Office Hours</h3>
            <p>Monday - Friday: 9am - 5pm</p>
        </div>
        <div class="section">
            <h3>Links</h3>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Services</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </div>
        <div class="section">
            <h3>Socials</h3>
            <ul>
                <li><a href="#"><i class="fab fa-facebook"></i></a></li>
                <li><a href="#"><i class="fab fa-twitter"></i></a></li>
                <li><a href="#"><i class="fab fa-instagram"></i></a></li>
            </ul>
        </div>
    </div>
</template>

<script setup>
</script>

<style scoped>
.footer {
    background-color: #f5f5f5;
    padding: 20px;
    text-align: center;
    display: flex;
    flex-direction: row;
    width: 100%;
    justify-content: space-between;
    background-color: #451d03;
}

.section {
    width: 20vw;
    margin-bottom: 20px;
   color: #fff;
   display: flex;
   flex-direction: column;
}

h3 {
    font-size: 18px;
    margin-bottom: 10px;
    color: #fff;
}

ul {
    list-style: none;
    padding: 0;
    margin: 0;
    color: #fff;
    display: flex;
   flex-direction: column;
}

li {
    display: inline-block;
    margin-right: 10px;
    color: #fff;
}

a {
    color: #fff;
    text-decoration: none;
}

a:hover {
    color: #666;
}


</style>