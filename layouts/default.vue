<template>
  <v-app dark>
    <!-- แถบด้านบน -->
    <v-app-bar app dark style="background: linear-gradient(90deg,rgb(32, 3, 3) 0%,rgb(32, 3, 3) 100%); box-shadow: 0 2px 12px rgba(0, 0, 0, 0.12);">
      <v-toolbar-title>Computer Technology</v-toolbar-title>
      <v-spacer></v-spacer>
      <!-- ปุ่ม hamburger สำหรับเปิดเมนูด้านขวา -->
      <v-app-bar-nav-icon @click="drawer = !drawer" right></v-app-bar-nav-icon>
    </v-app-bar>

    <!-- แถบเมนูด้านขวา -->
    <v-navigation-drawer
      v-model="drawer"
      right 
      temporary
      app
      dark  
      style="background-color:rgb(0, 0, 0) !important; color: #fff; box-shadow: 0 4px 24px rgb(0, 0, 0); border-top-left-radius: 18px; border-bottom-left-radius: 18px;"
    >
      <v-list>
        <v-list-item link to="/">
          <v-list-item-title class="menu-link">Home</v-list-item-title>
        </v-list-item>
        <v-list-item link to="/about">
          <v-list-item-title class="menu-link">About</v-list-item-title>
        </v-list-item>
        <v-list-item link to="/signup">
          <v-list-item-title class="menu-link">Signup</v-list-item-title>
        </v-list-item>
        <v-list-item link to="/login">
          <v-list-item-title class="menu-link">Login</v-list-item-title>
        </v-list-item>
        <v-list-item link to="/product">
          <v-list-item-title class="menu-link">Education</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

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
</style>