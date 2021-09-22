<template>
  <ul class="nav-list">
    <li class="nav-item"><nuxt-link to="/">Home</nuxt-link></li>
    <li class="nav-item"><nuxt-link to="/form">Enquiry Form</nuxt-link></li>
    <li class="nav-item"><nuxt-link to="/about">About</nuxt-link></li>
  </ul>
</template>

<style scoped>
.nav-list {
  list-style: none;
  padding: 0;
  margin: 0;
}

.nav-item {
  margin: 0 10px;
}

.nav-item a {
  text-decoration: none;
  color: black;
  font-size: 20px;
}

.nav-item a:hover,
.nav-item a:active {
  color: rgb(233, 199, 138);
}

@media (max-width: 991px) {
  .nav-list {
    display: block;
  }
  .nav-item {
    margin-top: 16px;
    margin-bottom: 16px;
  }
}

@media (min-width: 991px) {
  .nav-list {
    display: flex;
  }
}
</style>