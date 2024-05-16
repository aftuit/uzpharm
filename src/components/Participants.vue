<template>
  <div class="participants">
    <div class="container">
      <div class="header flex justify-between items-center">
        <div class="title">Participants</div>
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

      <div class="members flex">
        <div class="member-wrapper" v-for="n in 7" :key="n">
          <div class="members_item">
            <div class="img">
              <img src="https://admin.uzpharmforum.com/media/post/images/Rectangle-5-(1).png" alt="gerb" />
            </div>
            <div class="text text-dark">Ministry of Investment, Industry and Trade of the Republic of Uzbekistan</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.participants {
  padding: 280px 0 160px;
}
.members {
  margin-left: -12px;
  margin-right: -12px;
  row-gap: 24px;
  flex-wrap: wrap;
}
.member-wrapper {
  width: 25%;
  padding: 0 10px;
}
.members_item {
  align-items: flex-start;
  background-color: #ebf2f0;
  border-radius: 20px;
  display: flex;
  flex-direction: column;
  gap: 20px;
  height: 100%;
  padding: 24px;
}
.members_item .text {
  font-size: 20px;
  font-weight: 500;
  line-height: 150%;
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

@media (max-width: 1220px) {
  .member-wrapper {
    width: 33.33%;
  }
}
@media (max-width: 1000px) {
  .member-wrapper {
    width: 50%;
  }
  .participants {
    padding: 80px 0;
  }
}
@media (max-width: 700px) {
  .member-wrapper {
    width: 100%;
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
