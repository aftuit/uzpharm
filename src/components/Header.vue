<script setup>
import Navbar from "./Navbar.vue";
</script>

<template>
  <Navbar />
  <div class="section">
    <div class="container">
      <div class="main-content">
        <div class="wrapper first-section-wrapper">
          <h1 class="text-white">The Third International Pharmaceutical Forum of Uzbekistan</h1>
        </div>
        <div class="main-content-subtitle">
          <p class="text-white">
            The largest international event dedicated to solving the most pressing problems of the pharmaceutical industry of the new
            Uzbekistan
          </p>
        </div>

        <div class="flex gap-3 items-center infos">
          <div class="flex items-center gap-3 btn-items">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              fill="none"
              viewBox="0 0 32 32"
              class="t-icon t-icon-svg t-icon-clock"
              style="width: 32px; height: 32px; flex: 32px 0 0; fill: transparent; stroke: transparent">
              <path fill="#07A47F" d="M27 17a11 11 0 1 1-22 0 11 11 0 0 1 22 0"></path>
              <path
                fill="#1DDDAF"
                d="M16 5a12 12 0 1 0 12 12A12.014 12.014 0 0 0 16 5m0 22a10 10 0 1 1 10-10 10.01 10.01 0 0 1-10 10m5.708-15.707a1 1 0 0 1 0 1.415l-5 5a1 1 0 0 1-1.415-1.415l5-5a1 1 0 0 1 1.415 0M12 2a1 1 0 0 1 1-1h6a1 1 0 1 1 0 2h-6a1 1 0 0 1-1-1"></path>
            </svg>
            <span>May 30-31, 2024</span>
          </div>
          <div class="flex items-center gap-3 btn-items">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="32"
              height="32"
              fill="none"
              class="t-icon t-icon-svg t-icon-location"
              style="width: 32px; height: 32px; flex: 32px 0 0; fill: transparent; stroke: transparent">
              <path
                fill="#07A47F"
                d="M19.77 21.961a1 1 0 0 0-.17-.014h-7.2q-.086 0-.17.014C8.856 22.545 7 23.744 7 25.333 7 27.853 11.665 29 16 29s9-1.147 9-3.667c0-1.589-1.857-2.788-5.23-3.372"></path>
              <path
                fill="#1DDDAF"
                d="M16 3.381c-4.963 0-9 4.038-9 9 0 6.215 4.879 13.571 9 13.571s9-7.356 9-13.57c0-4.963-4.037-9-9-9m0 13.428a4.43 4.43 0 0 1-4.428-4.428A4.435 4.435 0 0 1 16 7.952a4.434 4.434 0 0 1 4.428 4.43A4.433 4.433 0 0 1 16 16.808m2.428-4.428A2.43 2.43 0 0 1 16 14.81a2.43 2.43 0 0 1-2.428-2.428c0-1.338 1.09-2.429 2.428-2.429a2.43 2.43 0 0 1 2.428 2.43"></path>
            </svg>
            <span>InterContinental Tashkent - Shakhrisabz Street 2</span>
          </div>
        </div>
      </div>
      <div class="extra-content flex justify-center items-center">
        <div class="img-wrapper">
          <img src="../assets/images/extra-1.png" alt="" />
        </div>
        <div class="extra-content-info">
          <h2>International Pharmaceutical Forum of Uzbekistan</h2>
          <p>
            The First International Pharmaceutical Forum of Uzbekistan declared itself to be a unique professional international platform
            for the leaders of the pharmaceutical industry, with the participation of the heads of the largest manufacturers, distributors,
            regulators, licensors of production technologies, lawyers and consulting specialists working in this field and many others.
          </p>
        </div>
        <div class="img-wrapper">
          <img src="../assets/images/extra-2.png" alt="" />
        </div>
      </div>
      <div class="main-counts flex items-center justify-center gap-5">
        <div class="card" v-for="n in 3" :key="n">
          <div class="count"><span>2 days</span></div>
          <div class="title"><span>BUSINESS COMMUNICATION AND NETWORKING</span></div>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
.main-counts {
  padding-bottom: 24px;
  gap: 30px;
  position: absolute;
  bottom: -10%;
  left: 4%;
 right: 4%;
}
.main-counts .card {
  align-items: center;
  background-color: var(--light-green);
  border-radius: 20px;
  display: flex;
  flex-direction: column;
  height: 230px;
  justify-content: center;
  overflow: hidden;
  padding: 34px 40px;
  position: relative;
  color: #fff;
}
.card .count {
  margin-bottom: 10px;
  text-align: center;
  font-family: Gilroy-Bold, sans-serif;
  font-size: 56px;
  font-weight: 600;
  line-height: 140%;
}
.card .title {
  text-align: center;
  font-size: 24px;
  font-weight: 400;
  line-height: 150%;
}
.main-counts .card::after {
  background-image: url("../assets/images/x.png");
  background-repeat: no-repeat;
  background-size: 100%;
  content: "";
  height: 140px;
  opacity: 0.1;
  position: absolute;
  right: 5px;
  top: 50%;
  transform: translate(25%, -50%) rotate(135deg);
  width: 140px;
}
.section {
  background-color: #044636;
  position: relative;
}
.main-content {
  align-items: center;
  display: flex;
  flex-direction: column;
  padding: 260px 0 280px;
  position: relative;
  z-index: 1;
  margin-bottom: 0.5em;
}
.main-content h1 {
  font-size: 70px;
  font-weight: 700;
  line-height: 120%;
  text-align: center;
  margin-bottom: 0.5em;
}
.main-content-subtitle {
  margin-bottom: 36px;
  max-width: 725px;
}
.main-content-subtitle p {
  font-size: 20px;
  font-weight: 400;
  line-height: 150%;
  text-align: center;
}
.first-section-wrapper {
  position: relative;
}
.btn-items {
  border: none;
  border-radius: 20px;
  cursor: pointer;
  outline: none;
  padding: 14px 24px;
  background-color: #ffffff1a;
}
.btn-items span {
  font-size: 24px;
  font-weight: 500;
  line-height: 150%;
  color: white;
  text-align: center;
}

.extra-content {
  margin: 0 -12px 80px;
  padding-bottom: 280px;
  gap: 30px;
}
.extra-content-info {
  width: 45%;
  color: white;
  text-align: center;
}
.extra-content-info h2 {
  font-size: 32px;
  text-wrap: wrap;
  line-height: 140%;
  font-weight: 500;
  margin-bottom: 0.5em;
}
.extra-content-info p {
  font-size: 20px;
  font-weight: 400;
  line-height: 150%;
  opacity: 0.8;
  text-align: center;
}

.img-wrapper {
  border-radius: 16px;
  height: 278px;
  overflow: hidden;
}
.img-wrapper img {
  height: 100%;
  object-fit: cover;
  object-position: center;
  width: 100%;
}
@keyframes toBig {
  1% {
    background-size: 0;
    opacity: 0;
  }
  40% {
    background-position: bottom;
  }
  100% {
    background-position: top;
    background-size: 100%;
    opacity: 1;
  }
}

@media (max-width: 1140px) {
  .main-content {
    padding: 130px 0;
  }
  .main-content h1 {
    font-size: 60px;
  }
}
@media (max-width: 960px) {
  .main-counts {
    flex-direction: column;
    justify-content: center;
    position: relative;
    left: auto;
    right: auto;
  }
  .main-counts .count {
    font-size: 46px;
  }
  .infos {
    flex-direction: column;
    justify-content: center;
  }
  .btn-items span {
    font-size: 18px;
  }
  .extra-content {
    flex-direction: column;
    gap: 35px;
    padding-bottom: 50px;
  }
  .extra-content .img-wrapper,
  .extra-content-info {
    width: 100%;
  }
}
@media (max-width: 576px) {
  .main-counts .count {
    font-size: 36px;
  }
  .main-content h1 {
    font-size: 36px;
  }
  .main-content p {
    font-size: 20px;
  }
}
</style>
