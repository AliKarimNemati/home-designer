<template>
    <section class="p-5">
        <h1 class="text-uppercase text-center">Our products</h1>
        <p class="text-center col-md-6 col-12 me-auto ms-auto">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
        tempor incididunt ut labore et dolore magna aliqua. Quis ipsum
        suspendisse ultrices gravida.</p>
        <div class="d-flex flex-wrap justify-content-center">
            <div class="col-md-2 col-10 ms-5 me-5">
                <div class="position-relative">
                    <img src="/img/calm-chair.jpg" class="product-img ">
                </div>
                <p class="text-center text-secondary mt-3">BLUE ARMCHAIR</p>
            </div>
            <div class="col-md-2 col-10 ms-5 me-5">
                <img src="/img/sofa.jpg" class="product-img">
                <p class="text-center text-secondary mt-3">GRAY SOFA</p>
            </div>
            <div class="col-md-2 col-10 ms-5 me-5">
                <img src="/img/planet.jpg" class="product-img">
                <p class="text-center text-secondary mt-3">ROPE POT</p>
            </div>
        </div>
        <div class="text-center">
            <router-link type="button" class="btn btn-secondary ps-4 pe-4 rounded-0" :to="{name: 'store'}">Shop Now</router-link>
        </div>
    </section>
</template>

<script>
export default {

}
</script>

<style lang="scss">
.product{
    &-img{
        border-radius: 50%;
        width: 100%;
    }
}
</style>
