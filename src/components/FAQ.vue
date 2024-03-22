<template>
  <div class="accordion-group">
    <h1 style="text-align: center; color: #451d03">FAQ</h1>
    <div class="accordion-list">
      <div class="item" v-for="(item, index) in accordionData" :class="{ active: isActive === index }">
        <a class="question" style="font-weight: bold" v-on:click="toggle(index)">
          <p>{{ item.question }}</p>
          <img class="icon" :src="'/plus.png'" alt="arrow"
            :class="{ 'icon': true, 'icon-status-hide': isActive === index, 'icon-status-show': isActive !== index }" />
          <img class="icon" :src="'/minus.png'" alt="arrow"
            :class="{ 'icon': true, 'icon-status-show': isActive === index, 'icon-status-hide': isActive !== index }" />
        </a>
        <div v-if="isActive === index" name="item" class="item-active">
          <p>{{ item.answer }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

const isActive = ref(0);
const accordionData = ref([
  {
    "question": "What areas do you serve in Rajasthan?",
    "answer": "We provide taxi services throughout Rajasthan, covering popular destinations such as Jaipur, Udaipur, Jodhpur, Pushkar, and many more."
  },
  {
    "question": "How do I make a booking?",
    "answer": "You can easily make a booking through our website by filling out the booking form, or you can contact us directly via phone or email to arrange your trip."
  },
  {
    "question": "Are your drivers experienced and licensed?",
    "answer": "Yes, all our drivers are experienced professionals with valid licenses. They are well-trained and knowledgeable about the local routes and attractions."
  },
  {
    "question": "What types of vehicles do you offer?",
    "answer": "We offer a range of vehicles to suit your needs, including sedans, SUVs, and minivans. Our fleet is well-maintained and regularly serviced to ensure your comfort and safety."
  },
  {
    "question": "Do you provide airport transfers?",
    "answer": "Yes, we offer airport transfer services for your convenience. Our drivers will be waiting for you at the airport upon your arrival and will ensure a smooth transfer to your destination."
  },
  {
    "question": "Can I customize my itinerary?",
    "answer": "Absolutely! We understand that every traveler has unique preferences, so we are happy to customize your itinerary according to your interests and schedule. Just let us know your requirements, and we'll tailor a package for you."
  }
]);

function toggle(index) {
  console.log("index", index);
  if (isActive.value === index) {
    isActive.value = null; // Allow deactivation
  } else {
    isActive.value = index;
  }
}
</script>

<style scoped>
.accordion-group {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-color: #fae4d4;
}

.accordion-group h1 {
  font-size: 3rem;
  color: #451d03;
}

.accordion-list {
  display: flex;
  flex-direction: column;
  width: 50%;
  margin-top: 2rem;
}

.item {
  width: 100%;
  margin: 1rem 0;
}

.question {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  position: relative;
}

.question:hover {
  background-color: transparent;
}

.question p {
  font-size: 1.75rem;
  color: #451d03;
}

.item-active p {
  color: #451d03;
  font-size: 1.25rem;
}


.item-active {
  animation: slideIn 0.5s ease-in-out;
}

@keyframes slideIn {
  0% {
    opacity: 0;
    transform: translateY(-40px);
  }

  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

.icon {
  height: 16px;
  width: 16px;
  margin: 0% 5%;
  position: absolute;
  right: 0;
}

.icon-status-hide {
  opacity: 0;
  transform: rotate(45deg);
  transition: all 0.5s;
}

.icon-status-show {
  opacity: 1;
  transition: all 0.5s;
}

@media (max-width: 768px) {

  .accordion-group {
    width: 100%;
    height: 100vh;
  }

  .accordion-list {
    width: 90%;
    margin-top: 1rem;
    margin-bottom: 1rem;
  }

  .question p {
    font-size: 1.5rem;
  }

  .item-active p {
    font-size: 1rem;
  }
}
</style>