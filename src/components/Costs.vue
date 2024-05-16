<script setup>
import { ref } from "vue";

const type = ref(1);

function getType(val) {
  type.value = val;
}
</script>

<template>
  <div class="costs">
    <div class="container">
      <div class="header">
        <h2>Cost and conditions of participation</h2>
      </div>

      <div class="price-buttons">
        <button :class="{ active: type == 1 }" @click="getType(1)">
          <span>Participation</span>
        </button>
        <button :class="{ active: type == 2 }" @click="getType(2)">
          <span>Become a partner</span>
        </button>
      </div>

      <div class="price_card">
        <div class="price_card-header"><h5>Cost</h5></div>
        <div class="price_card-body">
          <div class="price_card-price"><span> $1 500 </span></div>
          <div class="price_card-sub_title"><span>For one delegate</span></div>
          <div class="price_card-button">
            <button class="g-button g-button-kind-default g-button-color_kind-light">
              <div class="g-button-content"><span>Register</span></div>
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.costs {
  padding: 160px 0;
}
.header {
  gap: 32px;
  margin-bottom: 32px;
}
.header h2 {
  color: var(--text-dark);
  font-size: 48px;
  line-height: 150%;
  text-align: center;
}
.header p {
  text-align: center;
  font-size: 20px;
  font-weight: 400;
  line-height: 150%;
  color: #fff;
  opacity: 0.8;
}
.price-buttons {
  align-items: center;
  display: flex;
  justify-content: center;
  margin-bottom: 32px;
  gap: 10px;
}
.price-buttons button {
  border-radius: 20px;
  cursor: pointer;
  outline: none;
  padding: 14px 24px;
  align-items: center;
  display: flex;
  font-family: Gilroy-SemiBold, sans-serif;
  font-size: 20px;
  gap: 8px;
  line-height: 150%;
  background: transparent;
  border: 1px solid rgba(28, 47, 63, 0.2);
  font-weight: 500;
}
.price-buttons button.active {
  background: var(--light-green);
  border: 1px solid var(--light-green);
  color: #fff;
}

.price_card {
  border-radius: 20px;
  flex: 410px 1 1;
  max-width: 410px;
  overflow: hidden;
  width: 410px;
  margin: 0 auto;
}
.price_card-header {
  background-color: #0ac398;
  display: flex;
  justify-content: center;
  padding: 15px 0;
}
.price_card-header h5 {
  font-family: Gilroy-SemiBold, sans-serif;
  font-size: 20px;
  line-height: 150%;
  color: #fff;
}
.price_card-body {
  align-items: center;
  background-color: #07a781;
  display: flex;
  flex-direction: column;
  padding: 32px 0;
  position: relative;
  color: #fff;
}
.price_card-price {
  margin-bottom: 8px;
  z-index: 1;
  font-weight: 600;
}
.price_card-price span {
  font-family: Gilroy-Bold, sans-serif;
  font-size: 40px;
  line-height: 130%;
}
.price_card-sub_title {
  margin-bottom: 24px;
  z-index: 1;
}
.price_card-sub_title span {
  font-family: Gilroy-SemiBold, sans-serif;
  font-size: 24px;
  line-height: 130%;
}
.price_card-button {
  z-index: 1;
}
.price_card-button button {
  border: none;
  border-radius: 20px;
  cursor: pointer;
  outline: none;
  padding: 14px 24px;
  background: var(--light-green);
  align-items: center;
  display: flex;
  font-family: Gilroy-SemiBold, sans-serif;
  font-size: 20px;
  gap: 8px;
  color: #fff;
  line-height: 150%;
}
.price_card-body::after {
  background-image: url("../assets/images/x.png");
  background-repeat: no-repeat;
  background-size: 100%;
  content: "";
  height: 140px;
  left: 50%;
  opacity: 0.1;
  position: absolute;
  top: 20px;
  transform: translateX(-50%) rotate(135deg);
  width: 140px;
}
@media (max-width: 1000px) {
  .costs {
    padding: 80px 0;
  }
}
@media (max-width: 576px) {
  .header h2 {
    font-size: 34px;
  }
  .price_card-button button {
    border-radius: 16px;
    padding: 10px 24px;
    font-size: 18px;
  }
  .price-buttons button {
    border-radius: 16px;
    padding: 8px 18px;
    font-size: 17px;
  }
  .price_card {
    border-radius: 20px;
    flex: 300px 1 1;
    max-width: 300px;
    overflow: hidden;
    width: 300px;
    margin: 0 auto;
  }
}

@media (max-width: 450px) {
    .price-buttons{
        flex-direction: column;
    }
}
</style>
