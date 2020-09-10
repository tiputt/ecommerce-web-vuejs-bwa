<template>
  <div>
    <!-- Hero Section Begin -->
    <section class="hero-section">
      <carousel class="hero-items" :items="1" :nav="false" :autoplay="false">
        <div class="single-hero-items set-bg" style="background-image :url('/img/hero-1.jpg')">
          <div class="container">
            <div class="row">
              <div class="col-lg-5">
                <span>Outer</span>
                <h1>EXSTRA 25% OFF</h1>
                <h6>
                  KODE VOUCHER
                  <b>BYEAGUSTUS</b>
                </h6>
                <p>Syarat dan Ketentuan Berlaku</p>
                <a href="#" class="primary-btn">Shop Now</a>
              </div>
            </div>
          </div>
        </div>
        <div class="single-hero-items set-bg" style="background-image :url('/img/hero-2.jpg')">
          <div class="container">
            <div class="row">
              <div class="col-lg-5">
                <span>Shoes</span>
                <h1>KIDS FASHION</h1>
                <h3>Now on TazielShop</h3>
                <hr />
                <h6>
                  KODE VOUCHER
                  <b>BYEAGUSTUSKIDS</b>
                </h6>
                <p>Syarat dan Ketentuan Berlaku</p>
                <a href="#" class="primary-btn">Shop Now</a>
              </div>
            </div>
          </div>
        </div>
        <div class="single-hero-items set-bg" style="background-image :url('/img/hero-3.jpg')">
          <div class="container">
            <div class="row">
              <div class="col-lg-5">
                <span>Bag,kids</span>
                <h4>Spesial Fashion Payday Up to 70% Off +</h4>
                <h1>EXTRA OFF 40% OFF</h1>
                <p>Syarat dan Ketentuan Berlaku</p>
                <a href="#" class="primary-btn">Shop Now</a>
              </div>
            </div>
          </div>
        </div>
      </carousel>
    </section>
    <!-- Hero Section End -->
  </div>
</template>

<script>
import carousel from "vue-owl-carousel";

export default {
  name: "Carousel",
  components: {
    carousel,
  },
};
</script>

<style>
</style>