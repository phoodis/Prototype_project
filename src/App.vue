<template>
  <div>
    <Profile @edit-student="editStudent" />
    <Grades @edit-grades="editGrades" />
    <EditForm v-if="editing" :student="selectedStudent" />
  </div>
</template>

<script>
import Profile from "./components/Profile.vue";
import Grades from "./components/Grades.vue";
import EditForm from "./components/EditForm.vue";

export default {
  components: { Profile, Grades, EditForm },
  data() {
    return {
      editing: false,
      selectedStudent: null
    };
  },
  methods: {
    editStudent(student) {
      this.selectedStudent = student;
      this.editing = true;
    },
    editGrades(grades) {
      console.log("แก้ไขรายวิชา", grades);
    }
  }
};
</script>

<template>
  <div>
    <nav class="navbar">
      <router-link to="/" class="nav-link">🏠 Home</router-link>
      <router-link to="/about" class="nav-link">📖 About</router-link>
    </nav>
    <router-view />
  </div>
</template>

<style scoped>
.navbar {
  display: flex;
  justify-content: center;
  gap: 20px;
  background: #333;
  padding: 10px;
}
.nav-link {
  color: white;
  text-decoration: none;
  padding: 5px 10px;
}
.nav-link:hover {
  background: #555;
  border-radius: 5px;
}
</style>