<template>
    <div class="signup-form">
        <h2>สมัครสมาชิก</h2>
        <form @submit.prevent="submitForm">
            <div>
                <label for="username">ชื่อผู้ใช้</label>
                <input type="text" id="username" v-model="form.username" required />
            </div>
            <div>
                <label for="email">อีเมล</label>
                <input type="email" id="email" v-model="form.email" required />
            </div>
            <div>
                <label for="password">รหัสผ่าน</label>
                <input type="password" id="password" v-model="form.password" required />
            </div>
            <button type="submit">สมัครสมาชิก</button>
        </form>
    </div>
</template>

<script>
export default {
    data() {
        return {
            form: {
                username: '',
                email: '',
                password: ''
            }
        }
    },
    methods: {
        submitForm() {
            // ส่งข้อมูลไปยัง backend หรือแสดงผลลัพธ์
            alert('สมัครสมาชิกสำเร็จ!');
        }
    }
}
</script>

<style scoped>
.signup-form {
    max-width: 400px;
    margin: 40px auto;
    padding: 32px 28px 28px 28px;
    border-radius: 18px;
    background: #fff;
    box-shadow: 0 6px 32px 0 rgba(25, 118, 210, 0.10), 0 1.5px 6px 0 rgba(0,0,0,0.08);
    border: none;
    transition: box-shadow 0.3s;
}
.signup-form:hover {
    box-shadow: 0 10px 40px 0 rgba(25, 118, 210, 0.18), 0 2px 8px 0 rgba(0,0,0,0.10);
}
.signup-form h2 {
    text-align: center;
    margin-bottom: 28px;
    color:rgb(210, 25, 25);
    font-weight: 700;
    letter-spacing: 1px;
}
.signup-form div {
    margin-bottom: 20px;
}
.signup-form label {
    display: block;
    margin-bottom: 8px;
    color: #333;
    font-size: 15px;
    font-weight: 500;
}
.signup-form input {
    width: 100%;
    padding: 10px 12px;
    border: 1.5px solid #b0bec5;
    border-radius: 8px;
    font-size: 15px;
    transition: border-color 0.2s, box-shadow 0.2s;
    outline: none;
    background: #f8fafc;
    box-sizing: border-box;
}
.signup-form input:focus {
    border-color:rgb(255, 0, 0);
    box-shadow: 0 0 0 2px rgba(25, 118, 210, 0.10);
    background: #fff;
}
.signup-form button {
    width: 100%;
    padding: 12px;
    background: linear-gradient(90deg,rgb(255, 0, 0) 0%,rgb(0, 140, 255) 100%);
    color: #fff;
    border: none;
    border-radius: 8px;
    font-size: 17px;
    font-weight: 600;
    letter-spacing: 1px;
    cursor: pointer;
    box-shadow: 0 2px 8px 0 rgba(25, 118, 210, 0.10);
    transition: background 0.2s, box-shadow 0.2s;
}
.signup-form button:hover {
    background: linear-gradient(90deg,rgb(255, 0, 0) 0%,rgb(0, 128, 255) 100%);
    box-shadow: 0 4px 16px 0 rgba(25, 118, 210, 0.18);
}
</style>