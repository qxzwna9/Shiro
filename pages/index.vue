<template>
  <v-layout column justify-center align-center class="home-bg">
    <v-flex xs12>
      <div class="text-center">
        <VuetifyLogo />
      </div>

      <div class="text-center">
        <h1>ยินดีต้อนรับสู่ COMPUTER TECHNOLOGY WEBSITE</h1>

        <!-- ช่องอินพุต -->
        <v-text-field
          v-model="userMessage"
          label="พิมพ์ข้อความของคุณ"
          outlined
          class="mt-5"
        />

        <!-- แสดงข้อความ -->
        <h2>คุณพิมพ์ว่า: {{ userMessage }}</h2>

        <!-- แสดงรายการโพสต์ -->
        <v-container>
          <v-row>
            <v-col
              v-for="post in posts"
              :key="post.id"
              cols="12"
              sm="6"
              md="4"
            >
              <v-card class="post-card" outlined>
                <v-card-title>
                  <v-avatar size="44" class="mr-3" color="#8f0909">
                    <span class="white--text" style="font-weight:bold; font-size:1.2rem;">{{ post.title.charAt(0).toUpperCase() }}</span>
                  </v-avatar>
                  <div class="post-title-group">
                    <div class="post-title">{{ post.title }}</div>
                    <div class="post-id">#{{ post.id }}</div>
                  </div>
                </v-card-title>
                <v-card-text class="post-body">{{ post.body }}</v-card-text>
              </v-card>
            </v-col>
          </v-row>
        </v-container>

      </div>
    </v-flex>
  </v-layout>
</template>

<script>
import axios from 'axios'
import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  components: {
    VuetifyLogo
  },
  data() {
    return {
      userMessage: '', 
      posts: []        
    }
  },
  mounted() {
    axios.get('https://jsonplaceholder.typicode.com/posts')
      .then(response => {
        this.posts = response.data
      })
      .catch(error => {
        console.error('เกิดข้อผิดพลาดในการดึงข้อมูลโพสต์:', error)
        
      })
  }
}
</script>

<style scoped>
.home-bg {
  min-height: 100vh;
  background: linear-gradient(120deg,rgb(0, 0, 0) 0%,rgb(255, 0, 0) 100%);
  padding-top: 32px;
  padding-bottom: 32px;
}
.post-card {
  border-radius: 16px !important;
  box-shadow: 0 4px 18px rgba(255, 255, 255, 0.1);
  transition: box-shadow 0.2s, transform 0.2s;
  background: rgba(0, 0, 0, 0);
  min-height: 180px;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  border: 1.5px solidrgb(0, 0, 0);
}
.post-card:hover {
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.18);
  transform: translateY(-4px) scale(1.03);
  border: 1.5px solidrgb(255, 255, 255);
}
.post-title-group {
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.post-title {
  font-size: 1.1rem;
  font-weight: 600;
  color: #ffffff !important;
  margin-bottom: 2px;
  word-break: break-word;
}
.post-id {
  font-size: 0.92rem;
  color: #ffffff !important;
}
.post-body {
  color: #ffffff !important;
  font-size: 1.01rem;
  margin-top: 0.5rem;
  word-break: break-word;
}
</style>
