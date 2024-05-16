<template>
  <div style="background-color: #ffffff" class="hero_area">
    <svg
      class="waves"
      xmlns="http://www.w3.org/2000/svg"
      xmlns:xlink="http://www.w3.org/1999/xlink"
      viewBox="0 24 150 28"
      preserveAspectRatio="none"
      shape-rendering="auto">
      <defs><path id="gentle-wave" d="M-160 44c30 0 58-18 88-18s 58 18 88 18 58-18 88-18 58 18 88 18 v44h-352z"></path></defs>
      <g class="parallax">
        <use xlink:href="#gentle-wave" x="48" y="0" fill="#C1EDE2"></use>
        <use xlink:href="#gentle-wave" x="48" y="3" fill="#E0F6F1"></use>
      </g>
    </svg>
  </div>
  <div class="organizers">
    <div class="container">
      <h2>Organizers of the Forum</h2>

      <div class="organizer-group flex justify-center gap-5">
        <div class="organizers_item" v-for="n in 3" :key="n">
          <div class="img"><img src="https://admin.uzpharmforum.com/media/post/images/Rectangle-5-(1)-1681479954.png" alt="gerb" /></div>
          <div class="text text-dark">The Ministry of Health of the Republic of Uzbekistan</div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.organizers {
  background: var(--light);
  padding: 160px 0;
}
.organizers h2 {
  text-align: center;
  color: var(--text-dark);
  font-size: 48px;
  line-height: 150%;
  margin-bottom: 32px;
}

.organizers_item {
  align-items: center;
  background-color: #fff;
  border-radius: 20px;
  display: flex;
  flex-direction: column;
  gap: 16px;
  height: 100%;
  padding: 24px;
  text-align: center;
}
.organizers_item .img {
  height: 100px;
  width: 100px;
}
.img > img {
  height: 100%;
  object-fit: cover;
  object-position: center;
  width: 100%;
}
.organizers_item .text {
  font-size: 20px;
  font-weight: 600;
  line-height: 150%;
}

@media (max-width: 1000px) {
  .organizer-group {
    flex-wrap: wrap;
    justify-content: start;
  }
  .organizers_item {
    width: 45%;
  }
}

@media (max-width: 767px) {
  .organizers_item {
    width: 100%;
  }
  .organizers {
    padding: 80px 0;
  }
  .organizers h2 {
    font-size: 32px;
  }
}
@media (max-width: 576px) {
}
</style>
