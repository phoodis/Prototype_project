<template>
    <div>
      <h2>ข้อมูลนิสิต</h2>
      <img :src="student.picture" alt="Profile Picture" width="100" />
      <p>ชื่อ: {{ student.name }}</p>
      <p>รหัสนิสิต: {{ student.id }}</p>
      <p>วิทยาเขต: {{ student.campus }}</p>
      <p>โรงเรียนเดิม: {{ student.school }}</p>
      <button @click="edit">แก้ไข</button>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        student: {}
      };
    },
    methods: {
      fetchStudent() {
        fetch("http://localhost:3000/students/6630250371")
          .then(res => res.json())
          .then(data => (this.student = data));
      },
      edit() {
        this.$emit("edit-student", this.student);
      }
    },
    mounted() {
      this.fetchStudent();
    }
  };
  </script>
  