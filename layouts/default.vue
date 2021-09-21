<template>
  <div class="app-container">
    <Header />

    <v-main class="app-content">
      <nuxt />
    </v-main>
  </div>
</template>

<script>
import Header from '~/components/Header'
// import Footer from '~/components/Footer'
// import SideNav from '~/components/SideNav'
export default {
  components: {
    Header,

    // Footer,
  },
}
</script>

<style>
html,
body {
  margin: 0;
  height: 100%;
  width: 100%;
}
.app-container {
  height: 100%;
  position: relative;
  display: grid;
  grid-template: auto 1fr auto / 1fr;
}
.app-content {
  min-height: 100vh;
  padding: 24px;
  display: grid;
  align-items: center;
  justify-items: center;
}
</style>