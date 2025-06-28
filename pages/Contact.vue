<template>
  <div class="about-bg">
    <v-container class="my-10">
      <div class="about-card">
        <h1 class="about-title">Contact</h1>
        <v-img
          src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRGOjLOkcFYKtC-xokP20IHL-9kakxqKSbFyw&s"
          width="160"
          height="160"
          class="about-img mx-auto mb-6"
          alt="Computer Technology"
        ></v-img>
        <div class="about-info mb-4">
          <div class="about-row"><span class="about-label">Name:</span><span class="about-value">Panyakorn Saejao</span></div>
          <div class="about-row"><span class="about-label">Age:</span><span class="about-value">20</span></div>
          <div class="about-row"><span class="about-label">Department:</span><span class="about-value">Computer Technology</span></div>
          <div class="about-row"><span class="about-label">Email:</span><span class="about-value">panyakornsaejao@gmail.com</span></div>
          <div class="about-row"><span class="about-label">Facebook:</span><span class="about-value"><a href="https://facebook.com/panyakorn.saejao" target="_blank" class="about-link">panyakorn.saejao</a></span></div>
          <div class="about-row"><span class="about-label">Phone:</span><span class="about-value">063-xxx-xxxx</span></div>
        </div>
      </div>
    </v-container>
  </div>
</template>

<script>
export default {
  name: 'AboutPage'
}
</script>

<style scoped>
.about-bg {
  min-height: 100vh;
  width: 100vw;
  position: absolute;
  top: 0;
  left: 0;
  background: linear-gradient(120deg, rgb(134, 14, 14) 0%, rgb(6, 8, 141) 100%);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 0;
}
.about-card {
  background: rgba(0, 0, 0, 0.95);
  border-radius: 22px;
  box-shadow: 0 6px 32px 0 rgba(255, 255, 255, 0.8), 0 1.5px 6px 0 rgb(255, 0, 0);
  padding: 48px 48px 44px 48px;
  max-width: 650px;
  margin: 0 auto;
  text-align: center;
}
.about-title {
  color:rgb(255, 255, 255);
  font-size: 2.1rem;
  font-weight: 700;
  margin-bottom: 18px;
  letter-spacing: 1px;
}
.about-img {
  border-radius: 50%;
  box-shadow: 0 2px 12px rgb(255, 255, 255);
  border: 4px solid #fff;
}
.about-info {
  font-size: 1.08rem;
  color:rgb(255, 255, 255);
  margin-bottom: 18px;
  display: flex;
  flex-direction: column;
  gap: 6px;
  align-items: flex-start;
}
.about-row {
  display: flex;
  width: 100%;
  justify-content: flex-start;
  align-items: center;
}
.about-label {
  font-weight: 600;
  color:rgb(255, 255, 255);
  margin-right: 12px;
  min-width: 110px;
  display: inline-block;
  text-align: right;
}
.about-value {
  flex: 1;
  display: inline-block;
  text-align: left;
  word-break: break-all;
}
.about-link {
  color: #1976d2;
  text-decoration: underline;
  transition: color 0.2s;
}
.about-link:hover {
  color: #8f0909;
}
.about-btn {
  font-size: 1.08rem;
  font-weight: 600;
  border-radius: 8px;
  padding: 10px 28px;
  background: linear-gradient(90deg, #e53935 0%, #1976d2 100%);
  color: #fff !important;
  box-shadow: 0 2px 8px 0 rgba(25, 118, 210, 0.10);
  transition: background 0.2s, box-shadow 0.2s;
}
.about-btn:hover {
  background: linear-gradient(90deg, #b71c1c 0%, #1565c0 100%);
  box-shadow: 0 4px 16px 0 rgba(25, 118, 210, 0.18);
}
</style>
