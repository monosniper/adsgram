<template>
  <section class="trust" data-aos="fade-up" data-aos-duration="400">
    <div class="container">
      <span class="trust__tag" data-aos="fade-up" data-aos-delay="25">
        {{ $t("trust.tag") }}
      </span>
      <h2 class="trust__title" data-aos="fade-up" data-aos-delay="50">
        {{ $t("trust.title") }}
      </h2>
      <p class="trust__subtitle" data-aos="fade-up" data-aos-delay="75">
        {{ $t("trust.subtitle") }}
      </p>
      <div class="trust__cards">
        <div class="trust__card trust__card--ton" data-aos="fade-up" data-aos-delay="100">
          <p class="trust__text">{{ $t("trust.card1") }}</p>
        </div>
        <div class="trust__card trust__card--automation" data-aos="fade-up" data-aos-delay="125">
          <p class="trust__text">{{ $t("trust.card2") }}</p>
        </div>
        <div class="trust__card trust__card--moderation" data-aos="fade-up" data-aos-delay="150">
          <p class="trust__text">{{ $t("trust.card3") }}</p>
        </div>
        <div class="trust__card trust__card--usdt" data-aos="fade-up" data-aos-delay="175">
          <p class="trust__text">{{ $t("trust.card4") }}</p>
        </div>
      </div>
    </div>
  </section>
</template>




<style lang="scss" scoped>
@use "@/assets/scss/vars" as *;

.trust {
  padding: 30px 0 0;
  background: $bg-color-1;

  .container {
    max-width: 1440px;
    margin: 0 auto;
    padding: 0 112px 200px;
    text-align: left;
  }

  &__tag {
    color: #005bff;
    font-size: 16px;
    font-weight: 600;
    display: block;
    margin-bottom: 12px;
  }

  &__title {
    font-size: 36px;
    font-weight: 700;
    color: #181D27;
    margin-bottom: 16px;
  }

  &__subtitle {
    font-size: 18px;
    max-width: 700px;
    margin-bottom: 56px;
  }

  &__cards {
    display: flex;
    gap: 32px;
    justify-content: space-between;
  }

  &__card {
    background: #fff;
    border-radius: 16px;
    width: 100%;
    height: 320px;
    padding: 24px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
    position: relative;
    overflow: hidden;
  }

  &__card--ton {
    justify-content: flex-start;
  }

  &__card--ton::after {
    content: "";
    position: absolute;
    bottom: 0;
    left: 0;
    width: 236px;
    height: 242px;
    background: url("/assets/images/card1.png") no-repeat center/cover;
  }

  &__card--automation {
    justify-content: flex-start;
    background-color: #fff;
    background-image: url("/assets/images/card2.png");
    background-repeat: no-repeat;
    background-position: bottom center;
    background-size: contain;
  }

  &__card--moderation {
    justify-content: flex-start;
    background-color: #fff;
  }

  &__card--moderation::after {
    content: "";
    left: 20px;
    position: absolute;
    bottom: 120px;
    width: 196.64px;
    height: 53.55px;
    background: url("/assets/images/card3.png") no-repeat center/cover;
  }

  &__card--usdt {
    justify-content: flex-start;
    background-color: #fff;
  }

  &__card--usdt::after {
    content: "";
    position: absolute;
    bottom: 42px;
    left: 50%;
    transform: translateX(-50%);
    width: 151px;
    height: 151px;
    background: url("/assets/images/card4.png") no-repeat center/contain;
  }

  &__icon {
    width: 80px;
    height: 80px;
    margin-bottom: 16px;
  }

  &__text {
    font-size: 18px;
    font-weight: 600;
    color: #181D27;
    text-align: left;
    position: relative;
    z-index: 2;
  }

  @media (max-width: 768px) {
    .container {
      padding: 0 16px;
      text-align: left;
      margin-bottom: 64px;
      margin-top: 64px;
    }

    .trust__title {
      font-size: 24px;
      font-weight: 700;
    }

    .trust__subtitle {
      font-size: 16px;
    }

    .trust__cards {
      display: flex;
      flex-direction: column;
      gap: 16px;
      align-items: flex-start;
    }

    .trust__card {
      width: 100%;
      height: 320px;
      padding: 20px;
      text-align: left;
      align-items: flex-start;
    }

    .trust__text {
      font-size: 20px;
      text-align: left;
    }
  }
}
</style>
<script setup lang="ts">
</script>