<template>
  <div class="home">
    <Header />
    <Carousel />
    <WomanBanner />
    <InstaTaziel />
    <div class="benefit-items m-5">
      <div class="row">
        <div class="col-lg-4">
          <div class="single-benefit">
            <div class="sb-icon">
              <img src="img/icon-1.png" alt />
            </div>
            <div class="sb-text">
              <h6>Free Shipping</h6>
              <p>For all order over 99$</p>
            </div>
          </div>
        </div>
        <div class="col-lg-4">
          <div class="single-benefit">
            <div class="sb-icon">
              <img src="img/icon-2.png" alt />
            </div>
            <div class="sb-text">
              <h6>Delivery On Time</h6>
              <p>If good have prolems</p>
            </div>
          </div>
        </div>
        <div class="col-lg-4">
          <div class="single-benefit">
            <div class="sb-icon">
              <img src="img/icon-1.png" alt />
            </div>
            <div class="sb-text">
              <h6>Secure Payment</h6>
              <p>100% secure payment</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <PartnerLogo />
    <Footer />
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";
import Header from "@/components/Header.vue";
import Carousel from "@/components/Carousel.vue";
import WomanBanner from "@/components/WomanBanner.vue";
import InstaTaziel from "@/components/InstaTaziel.vue";
import PartnerLogo from "@/components/PartnerLogo.vue";
import Footer from "@/components/Footer.vue";

export default {
  name: "Home",
  components: {
    Header,
    Carousel,
    WomanBanner,
    InstaTaziel,
    PartnerLogo,
    Footer,
  },
};
</script>
