<script setup>
import Header from "./components/Header.vue";
import Participants from "./components/Participants.vue";
import MainSpeakers from "./components/MainSpeakers.vue";
import Advantages from "./components/Advantages.vue";
import Program from "./components/Program.vue";
import FormPartners from "./components/FormPartners.vue";
import Organizers from "./components/Organizers.vue";
import Costs from "./components/Costs.vue";
import Footer from "./components/Footer.vue";
import Loader from "./components/Loader.vue";

import { ref } from "vue";

const loading = ref(true);

setTimeout(() => {
  loading.value = false;
}, 1000);
</script>

<template>
  <Loader v-if="loading" />
  <template v-else>
    <div>
      <Header />
      <Participants />
      <MainSpeakers />
      <Advantages />
      <Program />
      <FormPartners />
      <Organizers />
      <Costs />
      <Footer />
    </div>
    <div class="contact-form">
      <img src="./assets/images/comment.png" alt="" />
    </div>
  </template>
</template>

<style scoped>
.contact-form {
  width: 70px;
  height: 70px;
  position: fixed;
  bottom: 30px;
  right: 30px;
  z-index: 23;
}
.contact-form img {
  width: 100%;
  height: 100%;
}
</style>
