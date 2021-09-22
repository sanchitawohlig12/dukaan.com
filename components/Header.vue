
<template>
  <header>
    <div class="brand-name">
      <nuxt-link to="/">dukaan.com</nuxt-link>
    </div>

    <div
      class="drawer-toggle"
      role="button"
      @click="$store.dispatch('nav/toggleSidebar')"
    >
      <div class="bar"></div>
      <div class="bar"></div>
      <div class="bar"></div>
    </div>

    <div class="app-links">
      <app-links></app-links>
    </div>
  </header>
</template>

<script>
import AppLinks from '~/components/AppLinks'

export default {
  components: { AppLinks },
}
</script>

<style scoped>
header {
  display: grid;
  grid-template: 60px / auto 1fr;
  align-items: center;
  background-color: white;
  border: rgb(218, 125, 5) 5px solid;
}

.app-links {
  justify-self: end;
}

.brand-name {
  margin: 0 10px;
  font-size: 2.3rem;
  border-right: rgb(218, 125, 5) 5px solid;
  width: 200%;
  text-align: center;
  margin-left: -35%;
}

.brand-name a {
  text-decoration: none;
  color: black;
}

.drawer-toggle .bar {
  width: 90%;
  height: 2px;
  background-color: black;
}

.drawer-toggle {
  display: flex;
  justify-self: end;
  flex-direction: column;
  justify-content: space-around;
  height: 50%;
  width: 35px;
  padding-right: 16px;
  cursor: pointer;
}

@media (max-width: 991px) {
  header {
    padding: 0 16px;
  }
  header:nth-child {
    justify-self: end !important;
  }
  .app-links {
    display: none;
  }
}

@media (min-width: 991px) {
  header {
    padding: 0 64px;
  }
  .app-links {
    display: block;
  }
  .drawer-toggle {
    display: none;
  }
}
</style>
