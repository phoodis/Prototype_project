<template>
    <div>
      <h2>รายวิชา</h2>
      <ul>
        <li v-for="grade in grades" :key="grade.subject">
          {{ grade.subject }} - {{ grade.unit }} หน่วยกิต - เกรด {{ grade.grade }}
        </li>
      </ul>
      <button @click="editGrades">แก้ไข</button>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        grades: []
      };
    },
    methods: {
      fetchGrades() {
        fetch("http://localhost:3000/grades?studentId=6630250371")
          .then(res => res.json())
          .then(data => (this.grades = data));
      },
      editGrades() {
        this.$emit("edit-grades", this.grades);
      }
    },
    mounted() {
      this.fetchGrades();
    }
  };
  </script>
  