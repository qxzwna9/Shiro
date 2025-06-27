<template>
    <div class="product-page">
        <h1 class="title">ข้อมูลนักศึกษา</h1>
        <div class="product-list">
            <div class="product-card" v-for="product in products" :key="product.id">
                <img :src="product.image" :alt="product.name" class="product-image" />
                <h2 class="product-name">{{ product.name }}</h2>
                <p class="product-desc">{{ product.description }}</p>
                <div class="product-footer">
                    <div class="product-btn-group">
                      <button class="detail-btn">แสดงรายละเอียด</button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "ProductPage",
    data() {
        return {
            products: [
                {
                    id: 1,
                    name: "Panyakorn Saejao",
                    description: "รหัสนักศึกษา: 65010101\nสาขา: Computer Technology\nอายุ: 20 ปี",
                    image: "https://randomuser.me/api/portraits/men/32.jpg"
                },
                {
                    id: 2,
                    name: "Sudarat Wongchai",
                    description: "รหัสนักศึกษา: 65010102\nสาขา: Information Technology\nอายุ: 21 ปี",
                    image: "https://randomuser.me/api/portraits/women/44.jpg"
                },
                {
                    id: 3,
                    name: "Nattapong Meechai",
                    description: "รหัสนักศึกษา: 65010103\nสาขา: Software Engineering\nอายุ: 22 ปี",
                    image: "https://randomuser.me/api/portraits/men/65.jpg"
                }
            ]
        }
    }
}
</script>

<style scoped>
.product-page {
    max-width: 900px;
    margin: 40px auto;
    padding: 20px;
    background: #fff;
    border-radius: 18px;
    box-shadow: 0 4px 24px rgba(0,0,0,0.08);
}
.title {
    text-align: center;
    margin-bottom: 32px;
    color: #2d3748;
    font-size: 2.2rem;
    font-weight: bold;
}
.product-list {
    display: flex;
    flex-wrap: wrap;
    gap: 32px;
    justify-content: center;
}
.product-card {
    background: #f9fafb;
    border-radius: 14px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.06);
    width: 260px;
    padding: 18px;
    display: flex;
    flex-direction: column;
    align-items: center;
    transition: box-shadow 0.2s;
}
.product-card:hover {
    box-shadow: 0 6px 24px rgba(0,0,0,0.12);
}
.product-image {
    width: 100%;
    height: 160px;
    object-fit: cover;
    border-radius: 10px;
    margin-bottom: 14px;
}
.product-name {
    font-size: 1.2rem;
    font-weight: 600;
    margin: 8px 0 4px 0;
    color: #22223b;
}
.product-desc {
    font-size: 0.98rem;
    color: #4a5568;
    margin-bottom: 12px;
    text-align: center;
}
.product-footer {
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.product-price {
    color: #e53e3e;
    font-weight: bold;
    font-size: 1.1rem;
}
.product-btn-group {
  display: flex;
  gap: 8px;
}
.buy-btn {
    background: #3182ce;
    color: #fff;
    border: none;
    border-radius: 6px;
    padding: 6px 18px;
    cursor: pointer;
    font-size: 1rem;
    transition: background 0.2s;
}
.buy-btn:hover {
    background: #2563eb;
}
.detail-btn {
  background: #fff;
  color: #3182ce;
  border: 1.5px solid #3182ce;
  border-radius: 6px;
  padding: 6px 14px;
  cursor: pointer;
  font-size: 1rem;
  font-weight: 500;
  transition: background 0.2s, color 0.2s, border 0.2s;
}
.detail-btn:hover {
  background: #3182ce;
  color: #fff;
  border: 1.5px solid #2563eb;
}
</style>