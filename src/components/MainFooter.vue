<template>
  <footer class="bg-dark p-5">
    <router-link class="navbar-brand text-uppercase text-white fs-4" :to="{ name: 'home' }">
      naturehomedec
      <i class="bi bi-house"></i>
    </router-link>
    <div class="d-flex flex-wrap justify-content-around border-bottom pb-5">
      <div class="col-md-4 col-12 mt-5">
        <h3 class="text-uppercase text-light">CONTACT</h3>
        <form class="text-center">
          <div class="mb-3">
            <input
              type="email"
              class="form-control"
              placeholder="Email address"
              required
            />
          </div>
          <div class="mb-3">
            <input
              type="text"
              class="form-control"
              placeholder="Your Name"
              required
            />
          </div>
          <div class="mb-3">
            <textarea
              rows="8"
              class="w-100 p-2 form-control"
              placeholder="Your Message"
              required
            ></textarea>
          </div>
          <button type="submit" class="btn btn-secondary ps-4 pe-4 rounded-0">
            Send
          </button>
        </form>
      </div>
      <div class="col-md-4 col-12 mt-5">
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
            <router-link :to="{name: 'store'}" class="nav-link text-light ms-2">STORE</router-link>
          </li>
        </ul>
      </div>
    </div>
    <div class="pt-5 d-flex justify-content-between">
        <p class="text-light text-uppercase">CopyRight | naturehomedec</p>
        <div>
          <i class="bi bi-facebook text-light fs-3 ps-3"></i>
          <i class="bi bi-whatsapp text-light fs-3 ps-3"></i>
          <i class="bi bi-telegram text-light fs-3 ps-3"></i>
        </div>
    </div>
  </footer>
</template>
