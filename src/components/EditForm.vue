<template>
    <div>
      <h2>แก้ไขข้อมูล</h2>
      <label>ชื่อ:</label>
      <input v-model="student.name" />
      <label>รหัสนิสิต:</label>
      <input v-model="student.id" disabled />
      <button @click="save">บันทึก</button>
    </div>
  </template>
  
  <script>
  export default {
    props: ["student"],
    methods: {
      save() {
        fetch(`http://localhost:3000/students/${this.student.id}`, {
          method: "PUT",
          headers: { "Content-Type": "application/json" },
          body: JSON.stringify(this.student)
        }).then(() => alert("บันทึกข้อมูลเรียบร้อย"));
      }
    }
  };
  </script>
  