<template>
  <!-- Partner Logo Section Begin -->
  <div class="partner-logo">
    <div class="container">
      <carousel
        class="logo-carousel"
        :items="5"
        :nav="false"
        :autoplay="true"
        :dots="false"
        :loop="true"
        :responsiveClass="true"
        :autoplaySpeed="true"
        :autoplayTimeout="5000"
        :responsive="{
         0:{items:1},576:{items:2},768:{items:3},1200:{items:4},1500:{items:5}
  }"
      >
        <div class="logo-item">
          <div class="tablecell-inner">
            <img src="img/logo-carousel/logo-1.png" alt />
          </div>
        </div>
        <div class="logo-item">
          <div class="tablecell-inner">
            <img src="img/logo-carousel/logo-2.png" alt />
          </div>
        </div>
        <div class="logo-item">
          <div class="tablecell-inner">
            <img src="img/logo-carousel/logo-3.png" alt />
          </div>
        </div>
        <div class="logo-item">
          <div class="tablecell-inner">
            <img src="img/logo-carousel/logo-4.png" alt />
          </div>
        </div>
        <div class="logo-item">
          <div class="tablecell-inner">
            <img src="img/logo-carousel/logo-5.png" alt />
          </div>
        </div>
      </carousel>
    </div>
  </div>
  <!-- Partner Logo Section End -->
</template>

<script>
import carousel from "vue-owl-carousel";

export default {
  name: "PartnerLogo",
  components: {
    carousel,
  },
  // directives: {
  //   carousel: {
  //     inserted: function (el) {
  //       $(el)
  //         .owlCarousel({
  //           //loop: true,
  //           margin: 10,
  //           nav: true,
  //           responsive: {
  //             0: {
  //               items: 1,
  //             },
  //             600: {
  //               items: 3,
  //             },
  //           },
  //         })
  //         .trigger("to.owl.carousel", app.items.length);
  //       console.log("crousel inserted");
  //     },
  //   },
  // },
};
</script>