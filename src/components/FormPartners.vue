<template>
  <div class="partners">
    <div class="container">
      <h2>Forum Partners</h2>
      <div class="partner">
        <h3>General Partner</h3>
        <div class="flex justify-center mt-3 gap-5 item-wrapper">
          <div class="partner_item">
            <img src="../assets/images/partner.png" alt="" />
          </div>
        </div>
      </div>
      <div class="partner">
        <h3>General Partner</h3>
        <div class="flex justify-center mt-3 gap-5 item-wrapper">
          <div class="partner_item">
            <img src="../assets/images/partner.png" alt="" />
          </div>
          <div class="partner_item">
            <img src="../assets/images/partner.png" alt="" />
          </div>
        </div>
      </div>
      <div class="partner">
        <h3>General Partner</h3>
        <div class="flex justify-center mt-3 gap-5 item-wrapper">
          <div class="partner_item">
            <img src="../assets/images/partner.png" alt="" />
          </div>
          <div class="partner_item">
            <img src="../assets/images/partner.png" alt="" />
          </div>
          <div class="partner_item">
            <img src="../assets/images/partner.png" alt="" />
          </div>
          <div class="partner_item">
            <img src="../assets/images/partner.png" alt="" />
          </div>
          <div class="partner_item">
            <img src="../assets/images/partner.png" alt="" />
          </div>
          <div class="partner_item">
            <img src="../assets/images/partner.png" alt="" />
          </div>
          <div class="partner_item">
            <img src="../assets/images/partner.png" alt="" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
.partners {
  padding: 160px 0;
}
.partners h2 {
  text-align: center;
  color: var(--text-dark);
  font-size: 48px;
  line-height: 150%;
}
.partners h3 {
  text-align: center;
  color: var(--text-dark);
  font-size: 28px;
  line-height: 130%;
}
.partner {
  margin-top: 70px;
}
.partner .item-wrapper {
  flex-wrap: wrap;
}
.partner_item {
  border: 1px solid #c5d4e0;
  border-radius: 20px;
  height: 180px;
  padding: 20px;
  flex-shrink: 0;
}
.partner_item img {
  object-fit: contain;
  height: 100%;
  object-position: center;
  width: 100%;
}

@media (max-width: 530px) {
  .partner_item {
    width: 100%;
  }
  .partners {
    padding: 80px 0;
  }
  .partners h2 {
    font-size: 34px;
  }
}
</style>
