<template>
  <div class="product">
    <Header />
    <!-- Breadcrumb Section Begin -->
    <div class="breacrumb-section text-left">
      <div class="container">
        <div class="row">
          <div class="col-lg-12">
            <div class="breadcrumb-text product-more">
              <router-link to="/">
                <i class="fa fa-home"></i> Home
              </router-link>
              <span>Detail</span>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- Breadcrumb Section Begin -->
    <ProductPicZoom />
    <RelateProduct />
    <Footer />
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";
import Header from "@/components/Header.vue";
import Footer from "@/components/Footer.vue";
import ProductPicZoom from "@/components/ProductPicZoom.vue";
import RelateProduct from "@/components/RelateProduct.vue";

export default {
  name: "Home",
  components: {
    Header,
    Footer,
    ProductPicZoom,
    RelateProduct,
  },
};
</script>
