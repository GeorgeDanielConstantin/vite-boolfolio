<script>
export default {
  data() {
    return {};
  },

  props: {
    title: String,
  },
};
</script>

<template>
  <header>
    <nav class="navbar navbar-expand-lg">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">Vite Boolfolio</a>
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarNav"
          aria-controls="navbarNav"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav">
            <li class="nav-item d-flex">
              <router-link
                :to="{ name: 'Homepage' }"
                class="nav-link"
                aria-current="page"
                href="#"
              >
                Home
              </router-link>
              <router-link
                :to="{ name: 'Contacts' }"
                class="nav-link"
                aria-current="page"
                href="#"
              >
                Contacts
              </router-link>
            </li>
          </ul>
        </div>
      </div>
    </nav>
    <h1 class="text-center mt-5">{{ title }}</h1>
  </header>
</template>

<style lang="scss" scoped></style>
