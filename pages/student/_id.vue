<template>
  <div class="student-detail-bg">
    <div class="student-detail-card">
      <h1 class="student-title">Student ID: {{ studentId }}</h1>
      <p class="student-desc">แสดงรายละเอียดสำหรับรหัสนักศึกษา <b>{{ studentId }}</b></p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'StudentDetail',
  computed: {
    studentId() {
      return this.$route.params.id;
    }
  }
}
</script>

<style scoped>
.student-detail-bg {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  background: linear-gradient(120deg, rgb(134, 14, 14) 0%, rgb(6, 8, 141) 100%);
}
.student-detail-card {
  background: #fff; 
  border-radius: 18px;
  box-shadow: 0 4px 24px rgb(255, 0, 0);
  padding: 100px 100px;
  min-width: 380px;
  max-width: 480px;
  width: 100%;
  text-align: center;
}
.student-title {
  font-size: 2rem;
  color:rgb(0, 21, 255);
  margin-bottom: 18px;
}
.student-desc {
  font-size: 1.15rem;
  color: #333;
}
</style>
