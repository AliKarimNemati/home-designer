<template>
  <!-- Alert -->
  <div class="alert alert alert-success alert-dismissible fade show fixed-top" role="alert" v-if="showAlert">
    <strong>Purchases successfully completed</strong>
      <a
      class="ms-3 link-dark fs-5"
      data-bs-toggle="modal"
      data-bs-target="#shopingitems"
      href="#"
      >
      See total items
    </a>
    <button type="button" class="btn-close" data-bs-dismiss="alert" aria-label="Close"></button>
  </div>

  <!-- main section -->
  <img src="/img/our-work-img.jpg" class="w-100 mt-5 top-img" height="250" />
  <section class="p-md-5 p-2">
    <h1 class="text-uppercase text-center">Our products</h1>
    <p class="text-center col-md-6 col-12 me-auto ms-auto">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
      tempor incididunt ut labore et dolore magna aliqua. Quis ipsum suspendisse
      ultrices gravida.
    </p>
    <div class="d-flex flex-wrap justify-content-center">
      <div
        class="col-md-3 col-10 ms-4 me-4 mt-5 card p-4"
        v-for="product in products"
        :key="product.id"
      >
        <div class="position-relative">
          <img :src="product.imgSrc" class="product-img" />
        </div>
        <p class="text-center text-secondary mb-0 mt-3 text-uppercase">
          {{ product.name }}
        </p>
        <p class="text-secondary text-center p-2 m-0">{{ product.des }}</p>
        <p class="text-center text-secondary text-uppercase english-number">
          ${{ product.price }}
        </p>
        <div class="text-center">
          <button
            type="button"
            class="btn btn-secondary ps-4 pe-4 rounded-0"
            @click="handleBuying"
            :value="product.id"
          >
            Buy
          </button>
        </div>
      </div>
    </div>
  </section>

  <!-- Modal -->
  <div
    class="modal fade"
    id="shopingitems"
    data-bs-backdrop="static"
    data-bs-keyboard="false"
    tabindex="-1"
    aria-labelledby="staticBackdropLabel"
    aria-hidden="true"
  >
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title english-number" id="staticBackdropLabel">
            Items
          </h5>
          <button
            type="button"
            class="btn-close"
            data-bs-dismiss="modal"
            aria-label="Close"
          ></button>
        </div>
        <div class="modal-body">
            <!-- Thanks for your shoping alert -->
            <div class="alert alert alert-success alert-dismissible fade show fixed-top" role="alert" v-if="showThanks">
              <strong>Thanks for your shoping</strong>
              <button type="button" class="btn-close" data-bs-dismiss="alert" aria-label="Close"></button>
            </div>
          <div
            class="
              border-bottom
              d-flex
              flex-wrap
              justify-content-between
              mt-3
              p-3
            "
            v-for="item in items"
            :key="item.id"
          >
            <div class="d-flex">
              <button type="button" class="btn-close ps-3" aria-label="Close" @click="deleteItem" :value="item.id"></button>
              <h5 class="english-number">{{ item.name }}</h5>
            </div>
            <h5 class="english-number">{{ item.price }}</h5>
          </div>
          <div v-if="showTotal" class="text-center">
            <h5 class="mt-3 english-number p-3">Total: ${{ total }}</h5>
          </div>
          <div class="text-center m-5 p-3" v-if="showEmpty">
            <h5>Empty</h5>
          </div>
        </div>
        <div class="text-center" v-if="showTotal">
          <button class="btn btn-secondary ps-4 pe-4 rounded-0 mb-3" @click="HandleEndShoping">
            Buy
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      products: [],
      items: [],
      total: 0,
      showTotal: false,
      showEmpty: true,
      showAlert: false,
      showThanks: false
    }
  },
  async mounted () {
    this.products = (await (await fetch('data/db.json')).json()).products
  },
  methods: {
    handleBuying (e) {
      const id = parseInt(e.target.value)
      this.products.forEach((e) => {
        if (e.id === id) {
          this.items.push(e)
        }
      })
      this.total = 0
      this.items.forEach((item) => {
        this.total += parseInt(item.price)
      })
      if (this.items) {
        this.showTotal = true
        this.showEmpty = false
      } else {
        this.showEmpty = true
      }

      this.showAlert = true
      setInterval(() => {
        this.showAlert = false
      }, 5000)
    },

    HandleEndShoping () {
      this.showThanks = true
      this.items = []
      this.showTotal = false
      this.showEmpty = true
      setInterval(() => {
        this.showThanks = false
      }, 5000)
    },

    deleteItem (e) {
      const id = parseInt(e.target.value)
      this.items = this.items.filter((value) => { return value.id !== id })
      this.total = 0
      this.items.forEach((item) => {
        this.total += parseInt(item.price)
      })
    }
  }
}
</script>

<style lang="scss" scoped>
.top-img {
  filter: brightness(0.5);
}
.product-img {
  height: 20rem;
}
</style>
