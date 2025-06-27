<template>
  <v-layout column justify-center align-center>
    <v-flex xs12>
      <div class="text-center">
        <VuetifyLogo />
      </div>

      <div class="text-center">
        <h1>ยินดีต้อนรับสู่ COMPUTER TECHNOLOGY</h1>

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
              <v-card class="ma-2" outlined>
                <v-card-title class="headline">{{ post.title }}</v-card-title>
                <v-card-text>{{ post.body }}</v-card-text>
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
