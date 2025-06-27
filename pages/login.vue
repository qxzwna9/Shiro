<template>
    <div class="login-container">
        <form class="login-form" @submit.prevent="handleLogin">
            <h2>เข้าสู่ระบบ</h2>
            <div class="form-group">
                <label for="username">ชื่อผู้ใช้</label>
                <input type="text" id="username" v-model="username" required />
            </div>
            <div class="form-group">
                <label for="password">รหัสผ่าน</label>
                <input type="password" id="password" v-model="password" required />
            </div>
            <button type="submit">เข้าสู่ระบบ</button>
        </form>
    </div>
</template>

<script>
export default {
    data() {
        return {
            username: '',
            password: ''
        }
    },
    methods: {
        handleLogin() {
            // เพิ่มโค้ดสำหรับการล็อคอินที่นี่
            alert(`Username: ${this.username}\nPassword: ${this.password}`);
        }
    }
}
</script>

<style scoped>
.login-container {
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    background: linear-gradient(120deg, #e3f2fd 0%, #f5f6fa 100%);
}

.login-form {
    background: #fff;
    padding: 2.5rem 2.5rem 2rem 2.5rem;
    border-radius: 18px;
    box-shadow: 0 6px 32px 0 rgb(255, 0, 0), 0 1.5px 6px 0 rgba(0, 38, 255, 0.08);
    width: 340px;
    border: none;
    transition: box-shadow 0.3s;
}
.login-form:hover {
    box-shadow: 0 10px 40px 0 rgb(47, 0, 255), 0 2px 8px 0 rgb(0, 224, 37);
}

.login-form h2 {
    text-align: center;
    margin-bottom: 2rem;
    color:rgb(255, 0, 0);
    font-weight: 700;
    letter-spacing: 1px;
}

.form-group {
    margin-bottom: 1.5rem;
}

.form-group label {
    display: block;
    margin-bottom: 0.5rem;
    color: #333;
    font-size: 15px;
    font-weight: 500;
}

.form-group input {
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
.form-group input:focus {
    border-color: #1976d2;
    box-shadow: 0 0 0 2px rgba(25, 118, 210, 0.10);
    background: #fff;
}

button[type="submit"] {
    width: 100%;
    padding: 12px;
    background: linear-gradient(90deg, #1976d2 0%, #42a5f5 100%);
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
button[type="submit"]:hover {
    background: linear-gradient(90deg, #1565c0 0%, #1976d2 100%);
    box-shadow: 0 4px 16px 0 rgba(25, 118, 210, 0.18);
}
</style>