<template>
  <v-app dark>
    <!-- แถบด้านบน -->
    <v-app-bar app dark style="background: linear-gradient(90deg,rgb(0, 0, 0) 0%,rgb(0, 0, 0) 100%); box-shadow: 0 2px 12px rgba(0, 0, 0, 0.12); height: 64px;">
      <v-spacer></v-spacer>
      <nuxt-link class="menu-link large-menu" to="/">Home</nuxt-link>
      <nuxt-link class="menu-link large-menu" to="/contact">Contact</nuxt-link>
      <nuxt-link class="menu-link large-menu" to="/news">News</nuxt-link>
    </v-app-bar>

    <!-- เนื้อหา -->
    <v-main>
      <Nuxt />
    </v-main>

    <!-- Footer -->
    <v-footer fixed app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      drawer: false
    }
  }
}
</script>

<style scoped>
.menu-link {
  color: #fff !important;
  font-weight: 600;
  font-size: 17px;
  letter-spacing: 0.5px;
  transition: color 0.2s;
}
.menu-link:hover {
  color: #FFD600 !important;
}
.large-menu {
  font-size: 1.45rem !important;
  padding: 0 28px !important;
  min-width: 110px;
}
.large-title {
  font-size: 2.6rem !important;
  font-weight: 800;
  letter-spacing: 2px;
  color: #FFD600 !important;
}
</style>