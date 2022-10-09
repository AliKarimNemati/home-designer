<template>
  <img
    src="/img/our-work-img.jpg"
    class="w-100 mt-5 top-img"
    height="250"
  />
  <section class="p-5">
    <h1 class="text-uppercase text-center">Our products</h1>
    <p class="text-center col-md-6 col-12 me-auto ms-auto">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
      tempor incididunt ut labore et dolore magna aliqua. Quis ipsum suspendisse
      ultrices gravida.
    </p>
    <div class="d-flex flex-wrap justify-content-center">
        <div class="col-md-3 col-10 ms-4 me-4 mt-5 card p-4" v-for="product in products" :key="product.id">
          <div class="position-relative">
            <img :src="product.imgSrc" class="product-img" />
          </div>
          <p class="text-center text-secondary mt-3 text-uppercase">{{ product.name }}</p>
          <p class="text-center text-secondary text-uppercase english-number">{{ product.price }}</p>
            <div class="text-center">
                <button type="button" class="btn btn-secondary ps-4 pe-4 rounded-0">
                Buy
                </button>
            </div>
        </div>
    </div>
  </section>
</template>

<script>
export default {
  data () {
    return {
      products: []
    }
  },
  async mounted () {
    this.products = (await (await fetch('data/db.json')).json()).products
    console.log(this.products)
  }
}
</script>

<style lang="scss">
.top-img {
  filter: brightness(0.5);
}
.product-img{
    height: 20rem ;
}
</style>
