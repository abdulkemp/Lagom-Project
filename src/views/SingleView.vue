<template>
  <body>
    <NavBar />
    <section>
      <div v-if="product" data-aos="zoom-in">
        <h1 class="heading animate__animated animate__zoomInUp">Product</h1>
        <div class="container-fluid">
          <div class="" id="cards"></div>
          <div class="row">
            <div class="col-3 card g-1 my-2 mx-2">
              <div class="card-body">
                <img :src="product.image" alt="" />
                <h5 class="name">{{ product.prodName }}</h5>
                <p class="description">{{ product.prodDesc }}</p>
                <p class="price">R{{ product.price }}</p>
                <a href="#" class="btn btn-primary">Add to checkout </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </body>
</template>

<script>
import NavBar from '@/components/NavBar.vue';
export default {
  name: "SingleProduct",
  components: {
    NavBar
  },
  props: ['id'],
  computed: {
    product() {
      return this.$store.state.product;
    },
  },
  mounted() {
    this.$store.dispatch('fetchProduct', this.id);
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
/* section{
    padding-top: 5%;
} */
body {
  background-image: url(https://i.postimg.cc/tRzCjrd5/140-1403845-bunga-png-japanese-cherry-blossom-png.png);
  background-color: rgba(244, 182, 192, 0.714);
  background-size: center;
  background-repeat: no-repeat;
  /* min-height: 100vh; */
  /* padding-top: 70px; */
}
</style>