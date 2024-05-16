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
  <div class="speakers">
    <div class="container">
      <div class="header flex justify-between items-center">
        <div class="title">Main speakers</div>
        <button class="next flex items-center gap-2">
          See all
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 16 16"
            class="t-icon t-icon-svg t-icon-arrow-left"
            style="width: 16px; height: 16px; flex: 16px 0 0; fill: transparent; stroke: transparent">
            <path fill="#06B48B" d="M12.172 7 6.808 1.636 8.222.222 16 8l-7.778 7.778-1.414-1.414L12.172 9H0V7z"></path>
          </svg>
        </button>
      </div>
      <div class="speakers-group flex">
        <div class="speaker-wrapper" v-for="n in 8" :key="n">
          <div class="speakers_item">
            <div class="img"><img src="../assets/images/speaker.png" alt="gerb" /></div>
            <div class="content">
              <div class="text text-dark">Asilbek Khudayarov</div>
              <div class="position">Minister</div>
              <div class="footer text-dark"><span>Ministry of Health of the Republic of Uzbekistan</span></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.speakers {
  background: var(--light);
  padding: 200px 0;
}
.speakers-group {
  margin-left: -12px;
  margin-right: -12px;
  row-gap: 24px;
  flex-wrap: wrap;
}
.speaker-wrapper {
  width: 25%;
  padding: 0 10px;
}
.speakers_item {
  align-items: flex-start;
  border-radius: 20px;
  display: flex;
  flex-direction: column;
  height: 100%;
  overflow: hidden;
}
.speakers_item .img {
  border-radius: 20px;
  flex: 350px 0 0;
  height: 350px;
  overflow: hidden;
  width: 100%;
}
.speakers_item img {
  height: 100%;
  object-fit: cover;
  object-position: center;
  width: 100%;
}
.speakers_item .content .text {
  font-size: 20px;
  font-weight: 600;
  line-height: 150%;
  margin-bottom: 12px;
}
.speakers_item .content {
  background-color: #fff;
  border-radius: 20px;
  display: flex;
  flex: 100% 1 1;
  flex-direction: column;
  padding: 16px;
}
.speakers_item .content .position {
  color: #06b48b;
  font-size: 18px;
  font-weight: 600;
  line-height: 150%;
  margin-bottom: 16px;
}
.speakers_item .content .footer {
  border-top: 1px solid #c5d4e0;
  height: 85px;
  margin-bottom: 16px;
  margin-top: auto;
  padding-top: 16px;
  width: 100%;
}
.speakers_item .content .footer span {
  font-size: 18px;
  font-weight: 600;
  line-height: 150%;
  color: var(--text-dark);
  opacity: 0.8;
}
.header {
  margin-bottom: 32px;
}
.header .title {
  font-family: Gilroy-Bold, sans-serif;
  font-weight: 600;
  font-size: 48px;
  line-height: 150%;
  color: var(--text-dark);
}
.header button {
  background-color: transparent;
  color: var(--text-dark);
  border: 1px solid rgba(28, 47, 63, 0.2);
  border-radius: 20px;
  cursor: pointer;
  outline: none;
  padding: 14px 24px;
  font-size: 20px;
  line-height: 150%;
  font-weight: 500px;
}

@media (max-width: 1200px) {
  .speaker-wrapper {
    width: 33.33%;
  }
}
@media (max-width: 1000px) {
  .speaker-wrapper {
    width: 50%;
  }
}
@media (max-width: 700px) {
  .speaker-wrapper {
    width: 100%;
  }
  .speakers_item .content {
    width: 100%;
  }
  .speakers {
    padding: 40px 0;
  }
  .header {
    flex-direction: column;
  }
  .header .title {
    font-size: 34px;
  }
  .header button {
    margin-top: 25px;
    margin-bottom: 25px;
  }
}
</style>
