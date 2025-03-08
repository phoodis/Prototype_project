<template>
    <div class="container">
      <h1>📌 หน้าหลัก</h1>
      <p>ยินดีต้อนรับเข้าสู่ระบบ!</p>
      <router-link to="/about" class="btn">ไปที่ข้อมูลนิสิต</router-link>
    </div>
  </template>
  
  <style scoped>
  .container {
    text-align: center;
    padding: 20px;
  }
  .btn {
    display: inline-block;
    padding: 10px 20px;
    margin-top: 10px;
    background: #42b983;
    color: white;
    text-decoration: none;
    border-radius: 5px;
  }
  </style>
  