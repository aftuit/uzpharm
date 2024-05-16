<script setup>
import { ref } from "vue";

const openSide = ref(false);
</script>

<template>
  <div class="drop" v-if="openSide"></div>
  <div class="side-bar" :class="{ show: openSide }">
    <div class="side-bar-header">
      <div class="flex justify-between items-center px-3 py-3">
        <div>
          <a href="#">
            <div class="items-center gap-2 flex text-white">
              <div>
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  fill="none"
                  viewBox="0 0 60 60"
                  class="t-icon t-icon-svg t-icon-logo logo-icon"
                  style="width: 60px; height: 60px; flex: 60px 0 0; fill: transparent; stroke: transparent">
                  <path
                    fill="#06B48B"
                    d="M42.4 22.471c-1.473.897-2.934 1.859-4.349 2.792l-1.78 1.172c-4.25 2.8-8.408 2.791-12.71 0l-1.533-1.008c-1.551-1.027-3.175-2.088-4.825-3.044A9.565 9.565 0 0 0 3.157 27.86l-.023.073a7 7 0 0 0-.147.572 9 9 0 0 0-.095.449c-.02.107-.036.223-.05.335a9 9 0 0 0-.067.584q-.013.185-.019.37c-.004.123-.016.215-.016.322 0 .054.007.108.008.157 0 .229.016.457.034.685 0 .034 0 .069.009.107a9.58 9.58 0 0 0 3.053 6.174 9.6 9.6 0 0 0 6.409 2.53 10 10 0 0 0 5.323-1.61c2.108-1.308 4.177-2.67 5.749-3.703 4.492-2.939 8.847-2.952 13.313 0l.478.322a63 63 0 0 0 6.553 3.972 9.48 9.48 0 0 0 11.936-3.272 9.6 9.6 0 0 0-1.074-12.147A9.614 9.614 0 0 0 42.4 22.47"></path>
                  <path
                    fill="#06B48B"
                    d="M30.109 22.47a9.6 9.6 0 0 0 6.779-2.811 9.581 9.581 0 0 0-6.792-16.357h-.098a9.525 9.525 0 0 0-8.78 5.898 9.5 9.5 0 0 0-.715 3.643v.108a9.56 9.56 0 0 0 2.83 6.747 9.57 9.57 0 0 0 6.776 2.772M29.933 38.704h-.052a9.57 9.57 0 0 0-6.815 2.874 9.66 9.66 0 0 0 0 13.472 9.57 9.57 0 0 0 6.815 2.887h.052a9.63 9.63 0 0 0 6.645-2.903 9.617 9.617 0 0 0-6.645-16.33"></path>
                </svg>
              </div>
              <div>
                <span class="text-logo side">
                  Third International Pharmaceutical <br />
                  Forum of Uzbekistan
                </span>
              </div>
            </div></a
          >
        </div>
        <div class="burger" @click="openSide = false">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            fill="#fff"
            viewBox="0 0 256 256"
            class="t-icon t-icon-svg t-icon-x close-icon"
            style="width: 30px; height: 30px; flex: 0 0 30px; fill: #fff; stroke: transparent">
            <path
              d="M205.66 194.34a8 8 0 0 1-11.32 11.32L128 139.31l-66.34 66.35a8 8 0 0 1-11.32-11.32L116.69 128 50.34 61.66a8 8 0 0 1 11.32-11.32L128 116.69l66.34-66.35a8 8 0 0 1 11.32 11.32L139.31 128Z"></path>
          </svg>
        </div>
      </div>
    </div>
    <div class="line"></div>
    <div class="side-content p-4 flex flex-col">
      <nav class="side_navigation flex flex-col gap-4 items-start">
        <div class="side_navigation_item"><a href="#">Program</a></div>
        <div class="side_navigation_item"><a href="#">Participants</a></div>
        <div class="side_navigation_item"><a href="#">Media</a></div>
      </nav>

      <div class="side-footer flex gap-3">
        <button class="p-2 dropdown text-white flex items-center gap-2">
          <span>Rus</span>
        </button>
        <button class="p-2 dropdown text-white flex items-center gap-2">
          <span>ENG</span>
        </button>
        <button class="bg-light-green text-white">
          <span>Register</span>
        </button>
      </div>
    </div>
  </div>

  <header class="header header-main">
    <div class="container">
      <div class="wrapper">
        <div class="content">
          <div class="logo-wrapper">
            <a href="#">
              <div class="items-center gap-2 flex text-white">
                <div>
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    fill="none"
                    viewBox="0 0 60 60"
                    class="t-icon t-icon-svg t-icon-logo logo-icon"
                    style="width: 60px; height: 60px; flex: 60px 0 0; fill: transparent; stroke: transparent">
                    <path
                      fill="#06B48B"
                      d="M42.4 22.471c-1.473.897-2.934 1.859-4.349 2.792l-1.78 1.172c-4.25 2.8-8.408 2.791-12.71 0l-1.533-1.008c-1.551-1.027-3.175-2.088-4.825-3.044A9.565 9.565 0 0 0 3.157 27.86l-.023.073a7 7 0 0 0-.147.572 9 9 0 0 0-.095.449c-.02.107-.036.223-.05.335a9 9 0 0 0-.067.584q-.013.185-.019.37c-.004.123-.016.215-.016.322 0 .054.007.108.008.157 0 .229.016.457.034.685 0 .034 0 .069.009.107a9.58 9.58 0 0 0 3.053 6.174 9.6 9.6 0 0 0 6.409 2.53 10 10 0 0 0 5.323-1.61c2.108-1.308 4.177-2.67 5.749-3.703 4.492-2.939 8.847-2.952 13.313 0l.478.322a63 63 0 0 0 6.553 3.972 9.48 9.48 0 0 0 11.936-3.272 9.6 9.6 0 0 0-1.074-12.147A9.614 9.614 0 0 0 42.4 22.47"></path>
                    <path
                      fill="#06B48B"
                      d="M30.109 22.47a9.6 9.6 0 0 0 6.779-2.811 9.581 9.581 0 0 0-6.792-16.357h-.098a9.525 9.525 0 0 0-8.78 5.898 9.5 9.5 0 0 0-.715 3.643v.108a9.56 9.56 0 0 0 2.83 6.747 9.57 9.57 0 0 0 6.776 2.772M29.933 38.704h-.052a9.57 9.57 0 0 0-6.815 2.874 9.66 9.66 0 0 0 0 13.472 9.57 9.57 0 0 0 6.815 2.887h.052a9.63 9.63 0 0 0 6.645-2.903 9.617 9.617 0 0 0-6.645-16.33"></path>
                  </svg>
                </div>
                <div>
                  <span class="text-logo">
                    Third International Pharmaceutical <br />
                    Forum of Uzbekistan
                  </span>
                </div>
              </div></a
            >
          </div>
          <nav class="navigation flex items-center gap-4">
            <div class="navigation_item"><a href="#">Program</a></div>
            <div class="navigation_item"><a href="#">Participants</a></div>
            <div class="navigation_item"><a href="#">Media</a></div>
          </nav>
          <div class="flex gap-4 buttons-wrap">
            <button class="nav-button dropdown text-white flex items-center gap-2">
              <span>ENG</span
              ><svg
                xmlns="http://www.w3.org/2000/svg"
                width="12"
                height="8"
                fill="none"
                class="t-icon t-icon-svg t-icon-vector-down"
                style="width: 12px; height: 12px; flex: 12px 0 0; fill: transparent; stroke: transparent">
                <path stroke="#fff" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="m1 1.5 5 5 5-5"></path>
              </svg>
            </button>
            <button class="nav-button bg-light-green text-white">
              <span>Register</span>
            </button>
          </div>
          <div class="burger" @click="openSide = true">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="32"
              height="32"
              fill="#fff"
              viewBox="0 0 256 256"
              class="t-icon t-icon-svg t-icon-burger"
              style="width: 30px; height: 30px; flex: 30px 0 0; fill: #fff; stroke: transparent">
              <path
                d="M224 128a8 8 0 0 1-8 8H40a8 8 0 0 1 0-16h176a8 8 0 0 1 8 8M40 72h176a8 8 0 0 0 0-16H40a8 8 0 0 0 0 16m176 112H40a8 8 0 0 0 0 16h176a8 8 0 0 0 0-16"></path>
            </svg>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<style scoped>
.side-footer {
  margin-top: auto;
}
.side-footer button {
  border: none;
  border-radius: 20px;
  cursor: pointer;
  outline: none;
  padding: 12px 20px;
  font-family: Gilro-SemiBold, sans-serif;
  font-size: 16px;
  line-height: 90%;
}
.side-bar {
  width: 100%;
  background: #044636;
  height: 100%;
  position: fixed;
  z-index: 12;
  left: -100%;
  transition: all 0.2s linear;
}
.side-bar.show {
  left: 0;
}
.drop {
  position: fixed;
  background: rgba(0, 0, 0, 0.5);
  top: 0;
  bottom: 0;
  right: 0;
  left: 0;
  z-index: 10;
}

.side-bar-header {
  width: 100%;
  height: 100px;
}
.line {
  background: #fff;
  width: 100%;
  height: 1px;
}
.side-content {
  width: 100%;
  height: calc(100vh - 101px);
}

.header-main {
  background-color: #044636;
  padding: 30px 0;
}
.header-main .wrapper {
  position: relative;
  z-index: 1;
}
.content {
  align-items: center;
  justify-content: space-between;
  flex-wrap: nowrap;
  display: flex;
  flex-flow: row wrap;
  margin-left: -12px;
  margin-right: -12px;
  row-gap: 24px;
}
.logo-wrapper {
  max-width: 100%;
  min-height: 1px;
  position: relative;
  padding-left: 12px;
  padding-right: 12px;
}
.logo-wrapper a {
  background-color: transparent;
  cursor: pointer;
  outline: none;
  text-decoration: none;
  transition: color 0.3s;
}
.text-logo {
  font-size: 19px;
  font-weight: 500;
  line-height: 140%;
}
.navigation {
  padding-left: 12px;
  padding-right: 12px;
  gap: 40px;
}
.navigation a {
  color: white;
  text-decoration: none;
  font-size: 20px;
  font-weight: 400;
  line-height: 150%;
  display: block;
}
.side_navigation a {
  color: white;
  text-decoration: none;
  font-size: 20px;
  font-weight: 400;
  line-height: 150%;
}
.navigation a:hover {
  color: var(--light-green);
}
.side_navigation a:hover {
  color: var(--light-green);
}
.buttons-wrap {
  padding: 0 12px;
}
.nav-button {
  border: none;
  border-radius: 20px;
  cursor: pointer;
  outline: none;
  padding: 14px 24px;
  font-family: Gilro-SemiBold, sans-serif;
  font-size: 20px;
  line-height: 150%;
}
.dropdown {
  background-color: #ffffff1a;
}
.burger {
  cursor: pointer;
  display: none;
}

@media (max-width: 1140px) {
  .burger {
    display: block;
  }
  .navigation,
  .buttons-wrap {
    display: none;
  }
}

@media (max-width: 500px) {
  .text-logo {
    display: none;
  }
  .text-logo.side {
    display: block;
    font-size: 16px;
  }
}
</style>
