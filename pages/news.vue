<template>
    <div class="news-bg">
      <div class="news-page">
          <h1 class="title">ข่าวสาร</h1>
          <div class="news-list">
              <div class="news-card" v-for="item in news" :key="item.id">
                  <img :src="item.image" :alt="item.title" class="news-image" />
                  <h2 class="news-title">{{ item.title }}</h2>
                  <p class="news-desc">{{ item.description }}</p>
              </div>
          </div>
      </div>
    </div>
</template>

<script>
export default {
    name: "NewsPage",
    data() {
        return {
            news: [
                {
                    id: 1,
                    title: "เปิดรับสมัครนักศึกษาใหม่ ปีการศึกษา 2568",
                    description: "เปิดรับสมัครนักศึกษาใหม่ระดับปริญญาตรี หลักสูตรเทคโนโลยีสารสนเทศ ตั้งแต่วันนี้ถึง 31 กรกฎาคม 2568",
                    image: "https://images.unsplash.com/photo-1464983953574-0892a716854b?auto=format&fit=crop&w=400&q=80"
                },
                {
                    id: 2,
                    title: "ขอเชิญร่วมงานสัมมนาเทคโนโลยี AI",
                    description: "ขอเชิญนักศึกษาและผู้สนใจเข้าร่วมงานสัมมนาเทคโนโลยี AI ในวันที่ 15 สิงหาคม 2568 ณ ห้องประชุมใหญ่ อาคารเรียนรวม",
                    image: "https://images.unsplash.com/photo-1506744038136-46273834b3fb?auto=format&fit=crop&w=400&q=80"
                },
                {
                    id: 3,
                    title: "ประกาศผลสอบกลางภาค 2568",
                    description: "สามารถตรวจสอบผลสอบกลางภาค ปีการศึกษา 2568 ได้ที่เว็บไซต์ของคณะ ตั้งแต่วันที่ 10 กรกฎาคม 2568 เป็นต้นไป",
                    image: "https://images.unsplash.com/photo-1515378791036-0648a3ef77b2?auto=format&fit=crop&w=400&q=80"
                },
                {
                    id: 4,
                    title: "อบรมเชิงปฏิบัติการ IoT สำหรับเยาวชน",
                    description: "เปิดรับสมัครเยาวชนเข้าร่วมอบรม IoT ฟรี! วันที่ 20-22 กรกฎาคม 2568 ณ ห้องปฏิบัติการคอมพิวเตอร์ อาคาร 2",
                    image: "https://images.unsplash.com/photo-1519389950473-47ba0277781c?auto=format&fit=crop&w=400&q=80"
                },
                {
                    id: 5,
                    title: "กิจกรรมวันแม่แห่งชาติ 2568",
                    description: "ขอเชิญนักศึกษาและบุคลากรเข้าร่วมกิจกรรมวันแม่แห่งชาติ วันที่ 12 สิงหาคม 2568 ณ ลานกิจกรรมกลางแจ้ง",
                    image: "https://images.unsplash.com/photo-1503676382389-4809596d5290?auto=format&fit=crop&w=400&q=80"
                },
                {
                    id: 6,
                    title: "ทุนการศึกษาสำหรับนักศึกษาดีเด่น",
                    description: "เปิดรับสมัครขอรับทุนการศึกษาสำหรับนักศึกษาดีเด่น ประจำปี 2568 ตั้งแต่วันนี้ถึง 31 สิงหาคม 2568",
                    image: "https://images.unsplash.com/photo-1465101046530-73398c7f28ca?auto=format&fit=crop&w=400&q=80"
                }
            ]
        }
    }
}
</script>

<style scoped>
.news-bg {
    min-height: 100vh;
    width: 100vw;
    background: linear-gradient(90deg,rgb(134, 14, 14) 0%,rgb(6, 8, 141) 100%);
    display: flex;
    justify-content: center;
    align-items: flex-start;
    padding-top: 32px;
}
.news-page {
    max-width: 900px;
    width: 100%;
    margin: 0 auto 40px auto;
    padding: 20px;
    /* background: #fff; */
    border-radius: 18px;
    box-shadow: none;
}
.title {
    text-align: center;
    margin-bottom: 32px;
    color:rgb(0, 94, 255);
    font-size: 2.2rem;
    font-weight: bold;
}
.news-list {
    display: grid;
    grid-template-rows: repeat(2, 1fr);
    grid-template-columns: repeat(3, 1fr);
    gap: 32px;
    justify-content: center;
}
.news-card {
    background: rgba(0, 0, 0, 0.92);
    border-radius: 14px;
    box-shadow: 0 2px 12px rgba(0,0,0,0.10);
    width: 100%;
    max-width: 320px;
    padding: 18px;
    display: flex;
    flex-direction: column;
    align-items: center;
    transition: box-shadow 0.2s;
}
.news-image {
    width: 100%;
    height: 160px;
    object-fit: cover;
    border-radius: 10px;
    margin-bottom: 14px;
}
.news-title {
    font-size: 1.15rem;
    font-weight: 600;
    margin: 8px 0 4px 0;
    color:rgb(25, 0, 255);
    text-align: center;
}
.news-desc {
    font-size: 1.01rem;
    color:rgb(255, 255, 255);
    margin-bottom: 8px;
    text-align: center;
}
</style>