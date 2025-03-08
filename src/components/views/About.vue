<template>
    <div class="container">
      <h1>📖 ข้อมูลนิสิต</h1>
      <Profile />
      <Grades />
      <router-link to="/" class="btn">กลับหน้าหลัก</router-link>
    </div>
  </template>
  
  <script>
  import Profile from '@/components/Profile.vue';
  import Grades from '@/components/Grades.vue';
  
  export default {
    components: { Profile, Grades }
  };
  </script>
  
  <style scoped>
  .container {
    text-align: center;
    padding: 20px;
  }
  .btn {
    display: inline-block;
    padding: 10px 20px;
    margin-top: 10px;
    background: #ff7f50;
    color: white;
    text-decoration: none;
    border-radius: 5px;
  }
  </style>
  