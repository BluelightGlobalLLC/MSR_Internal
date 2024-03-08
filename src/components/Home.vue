<script setup>
import { ref } from 'vue';
import axios from 'axios';

const code = ref("")
const validity = ref("Enter code to check validity");
async function checkValidity() {
  try {
    const response = await axios.get(`https://b54b8e49-34c4-4275-b908-727aadc1e33b-00-157ri02fq3f13.spock.replit.dev/v1/check/${code.value}`);
    validity.value = response.data;
  } catch (error) {
    console.error(error);
  }
}
</script>

<template>
  <div class="wrapper">
    <div class="line"></div>
    <div class="centered">
      <img src="../assets/rewards.png" alt="Rewards" class="reward-icon">
      <h1 class="title">Shop at <span class="colored">M Souq</span> & Win exciting Rewards!</h1>
      <div class="content">
        <div class="subtitles">
          <h3 class="subtitle-1">Redeem M Souq rewards</h3>
          <h3 class="subtitle-2">Insert your promo code to avail exclusive offers</h3>
          <div class="input">
            <input type="text" v-model="code">
            <div class="button" @click="checkValidity">Check Coupon</div>
          </div>
          <h3 class="subtitle-1">Reward Validity</h3>
          <div class="output">
            <h3>{{ validity }}</h3>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.wrapper {
  height: 100%;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}

.line {
  width: 2rem;
  background-color: #0071c1;
  height: 40rem;
  -webkit-transform: translateY(-20px) translateX(5px) rotate(50deg);
  transform: translateY(-20px) translateX(5px) rotate(50deg);
  position: absolute;
  top: -10rem;
  left: 0;
}

.button {
  background-color: #0071c1;
  color: #fff;
  height: 100%;
  width: 20%;
  border-top-right-radius: 0.5rem;
  border-bottom-right-radius: 0.5rem;
  text-align: center;
  display: flex;
  justify-content: center;
  align-items: center;
  cursor: pointer;
}

.input {
  height: 2rem;
  width: 30rem;
  border-radius: 0.5rem;
  border: #CFCECF 1px solid;
  display: flex;
  justify-content: start;
  align-items: center;
  padding-left: 0.5rem;
  margin-bottom: 1.5rem;
}

.output {
  height: 2rem;
  width: 30rem;
  border-radius: 0.5rem;
  background-color: #E1EDEF;
  display: flex;
  justify-content: start;
  align-items: center;
  padding-left: 0.5rem;
  margin-bottom: 1.5rem;
  margin-top: 0.3rem;
  font-weight: 500;
}

input {
  height: 1.3rem;
  width: 80%;
  border: transparent;
  outline: transparent;
}

.centered {
  height: 25rem;
  width: 40rem;
  background-color: #fff;
  display: flex;
  align-items: center;
  text-align: center;
  flex-direction: column;
  padding: 2rem 1rem;
  color: rgb(28, 27, 27);
  font-size: 0.6rem;
  font-weight: 400;
}

.reward-icon {
  margin-top: 2rem;
  max-width: 5rem;
}

.colored {
  color: #0071c1;
}

.title {
  margin-bottom: 2rem;
}

.subtitles {
  display: flex;
  flex-direction: column;
  margin: 0;
  padding: 0;
}

.subtitle-1 {
  margin: 0;
  padding: 0;
  font-weight: 600;
  margin-bottom: 0.3rem;
  color: #0071c1;
  text-decoration: underline;
}

.subtitle-2 {
  margin: 0;
  padding: 0;
  font-weight: 500;
  margin-bottom: 0.5rem;
}

.content {
  width: 100%;
  height: max-content;
  display: flex;
  justify-content: start;
  text-align: start;
  font-weight: 700;
}
</style>
