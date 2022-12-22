<template>
  <section class="d-flex flex-wrap p-5 mt-5 ps-md-0">
    <div class="col-md-6 col-12 text-center">
      <img src="/img/main-img.jpg" class="main-img w-75" />
    </div>
    <div class="col-md-6 col-12 mt-md-0 mt-4">
      <p class="des text-uppercase text-center">new catalog</p>
      <h1 class="text-uppercase text-center">natural home decor</h1>
      <p class="des text-center">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua. Quis ipsum
        suspendisse ultrices gravida. Risus commodo viverra maecenas accumsan
        lacus vel facilisis.
      </p>
      <div class="text-center">
        <button
          type="button"
          class="btn btn-secondary ps-4 pe-4 rounded-0 text-center"
        >
        Read more
        </button>
      </div>
      <div class="text-center mt-4">
        <img src="/img/planet.jpg" class="rounded-circle w-50"/>
      </div>
    </div>
  </section>

  <section class="d-flex flex-wrap p-5">
    <div class="col-md-6 col-12 pe-md-5 ps-md-3 align-self-center text-center text-md-start">
      <h1 class="text-uppercase">Download our new catalog</h1>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua. Quis ipsum
        suspendisse ultrices gravida. Risus commodo viverra maecenas accumsan
        lacus vel facilisis.</p>
      <div>
        <button type="button" class="btn btn-secondary ps-4 pe-4 rounded-0">Download Now</button>
      </div>
    </div>
    <div class="col-md-6 col-12 mt-5 mt-md-0">
      <img src="/img/catalog.jpg" class="w-100 rounded">
    </div>
  </section>
  <OurProducts />
  <AboutUs />
  <NewMaterials />
  <CantactUs />

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
          <button
            type="button"
            class="btn-close"
            data-bs-dismiss="modal"
            aria-label="Close"
          ></button>
        </div>
        <div class="modal-body">
        </div>
        <div class="text-center">
          <a class="btn btn-secondary ps-4 pe-4 rounded-0 mb-3" href="/store">
            Buy Now
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import OurProducts from '../components/OurProdocts.vue'
import AboutUs from '../components/AboutUs.vue'
import NewMaterials from '../components/NewMaterials.vue'
import CantactUs from '../components/CantactUs.vue'
export default {
  name: 'HomeView',
  components: { OurProducts, AboutUs, NewMaterials, CantactUs }
}
</script>

<style lang="scss">
.main-img {
  border-radius: 330px 330px 30px 30px;
}
</style>
