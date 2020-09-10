<template>
  <div>
    <!-- Product Shop Section Begin -->
    <section class="product-shop spad page-details">
      <div class="container">
        <div class="row">
          <div class="col-lg-12">
            <div class="row">
              <div class="col-lg-6">
                <div class="product-pic-zoom">
                  <img class="product-big-img" :src="image_default" alt />
                </div>
                <div class="product-thumbs">
                  <carousel
                    class="product-thumbs-track ps-slider"
                    :autoplay="true"
                    :loop="true"
                    :items="3"
                    :nav="false"
                    :dots="false"
                    :responsiveClass="true"
                    :autoplaySpeed="true"
                    :autoplayTimeout="5000"
                    :responsive="{
         0:{items:1},576:{items:2},768:{items:3},1200:{items:4},1500:{items:5}
  }"
                  >
                    <div
                      class="pt"
                      @click="changeImage(thumbs[0])"
                      :class="thumbs[0] == image_default ? 'active' : '' "
                    >
                      <img src="img/zlr-product/cargo1.jpg" alt />
                    </div>

                    <div
                      class="pt"
                      @click="changeImage(thumbs[1])"
                      :class="thumbs[1] == image_default ? 'active' : '' "
                    >
                      <img src="img/zlr-product/cargo2.jpg" alt />
                    </div>

                    <div
                      class="pt"
                      @click="changeImage(thumbs[2])"
                      :class="thumbs[2] == image_default ? 'active' : '' "
                    >
                      <img src="img/zlr-product/cargo3.jpg" alt />
                    </div>
                  </carousel>
                </div>
              </div>
              <div class="col-lg-6">
                <div class="product-details text-left">
                  <div class="pd-title">
                    <span>{{productDetails.type}}</span>
                    <h3>{{productDetails.name}}</h3>
                  </div>
                  <div class="pd-desc">
                    <p>{{productDetails.description}}</p>
                    <h4>${{productDetails.price}}</h4>
                  </div>
                  <div class="quantity">
                    <router-link to="/shoppingcart" class="primary-btn pd-cart">Add To Cart</router-link>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- Product Shop Section End -->
  </div>
</template>

<script>
import carousel from "vue-owl-carousel";
import axios from "axios";

export default {
  name: "ProductPicZoom",
  components: {
    carousel,
  },
  data() {
    return {
      image_default: "img/zlr-product/cargo1.jpg",
      thumbs: [
        "img/zlr-product/cargo1.jpg",
        "img/zlr-product/cargo2.jpg",
        "img/zlr-product/cargo3.jpg",
      ],
      productDetails: [],
    };
  },
  methods: {
    changeImage(urlImage) {
      this.image_default = urlImage;
    },
  },
  mounted() {
    axios
      .get("http://shayna-backend.belajarkoding.com/api/products", {
        params: {
          id: this.$route.params.id,
        },
      })
      .then((res) => (this.productDetails = res.data.data))
      // eslint-disa  var console: Console le
      .catch((err) => console.log(err));
  },
};
</script>

<style>
</style>