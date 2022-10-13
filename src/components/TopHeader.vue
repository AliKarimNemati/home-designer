<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-dark">
    <div class="container-fluid">
      <router-link
        class="navbar-brand text-uppercase text-white fs-4"
        :to="{ name: 'home' }">
        naturehomedec
        <i class="bi bi-house"></i>
        </router-link
      >
      <button
        class="navbar-toggler bg-light"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav ms-auto me-1 mb-2 mb-lg-0">
          <li class="nav-item">
            <a href="/#contact" class="nav-link text-light ms-2">CONTACT</a>
          </li>
          <li class="nav-item">
            <a href="/#aboutUs" class="nav-link text-light ms-2">ABOUT US</a>
          </li>
          <li class="nav-item">
            <a href="/#materials" class="nav-link text-light ms-2">MATERIALS</a>
          </li>
          <li class="nav-item">
            <router-link
              :to="{ name: 'store' }"
              class="nav-link text-light ms-2"
              >STORE</router-link
            >
          </li>
          <button
            type="button"
            class="btn btn-secondary rounded-0"
            data-bs-toggle="modal"
            data-bs-target="#shopingitems"
          >
            <i class="bi bi-basket3"></i>
          </button>
        </ul>
      </div>
    </div>
  </nav>
</template>

<style lang="scss" scoped>
a.nav-link {
  font-size: 0.9rem !important;
  letter-spacing: 1px;
}
</style>
