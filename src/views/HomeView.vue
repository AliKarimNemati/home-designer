<template>
  <section class="d-flex flex-wrap p-5 ps-md-0">
    <div class="col-md-6 col-12 text-center">
      <img src="../assets/img/main-img.jpg" class="main-img w-75" />
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
        <img src="../assets/img/planet.jpg" class="rounded-circle w-50"/>
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
      <img src="../assets/img/catalog.jpg" class="w-100 rounded">
    </div>
  </section>
  <OurProducts />
  <AboutUs />
  <NewMaterials />
</template>

<script>
import OurProducts from '../components/OurProdocts.vue'
import AboutUs from '../components/AboutUs.vue'
import NewMaterials from '../components/NewMaterials.vue'
export default {
  name: 'HomeView',
  components: { OurProducts, AboutUs, NewMaterials }
}
</script>

<style lang="scss">
.main-img {
  border-radius: 40% 40% 0 0;
}
</style>
