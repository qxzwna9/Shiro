<template>
    <div class="product-detail-page">
        <h1>รายละเอียดนักศึกษา</h1>
        <div v-if="student">
            <img :src="student.image" :alt="student.name" class="product-detail-image" />
            <h2>{{ student.name }}</h2>
            <p>รหัสนักศึกษา: {{ student.studentId }}</p>
            <p>สาขา: {{ student.major }}</p>
            <p>อายุ: {{ student.age }} ปี</p>
            <p>รหัสหน้า: {{ id }}</p>
        </div>
        <div v-else>
            <p>ไม่พบข้อมูลนักศึกษานี้</p>
        </div>
    </div>
</template>

<script>
const students = [
    {
        id: '1',
        name: "Panyakorn Saejao",
        studentId: "65010101",
        major: "Computer Technology",
        age: 20,
        image: "https://randomuser.me/api/portraits/men/32.jpg"
    },
    {
        id: '2',
        name: "Sudarat Wongchai",
        studentId: "65010102",
        major: "Information Technology",
        age: 21,
        image: "https://randomuser.me/api/portraits/women/44.jpg"
    },
    {
        id: '3',
        name: "Nattapong Meechai",
        studentId: "65010103",
        major: "Software Engineering",
        age: 22,
        image: "https://randomuser.me/api/portraits/men/65.jpg"
    }
];

export default {
    async asyncData({ params }) {
        const student = students.find(s => s.id === params.id);
        return {
            id: params.id,
            student
        }
    }
}
</script>

<style scoped>
.product-detail-page {
    max-width: 500px;
    margin: 40px auto;
    background: #fff;
    border-radius: 18px;
    box-shadow: 0 4px 24px rgba(0,0,0,0.08);
    padding: 32px 24px;
    text-align: center;
}
.product-detail-image {
    width: 100%;
    max-width: 220px;
    height: 220px;
    object-fit: cover;
    border-radius: 50%;
    margin-bottom: 18px;
    box-shadow: 0 2px 12px rgba(0,0,0,0.10);
}
</style>