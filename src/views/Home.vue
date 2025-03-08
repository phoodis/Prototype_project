<template>
    <div class="home-container">
      <div class="overlay"></div>
      <h1>Welcome to Home Page</h1>
    </div>
  </template>
  
  <script>
  export default {
    name: "Home",
  };
  </script>
  
  <style scoped>
  .home-container {
    position: relative;
    width: 100%;
    height: 100vh;
    background: url("https://source.unsplash.com/random/1600x900") no-repeat center center/cover;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    color: white;
  }
  
  /* ✅ แก้ให้ overlay ไม่บังการคลิก */
  .overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5);
    pointer-events: none; /* ✅ ทำให้สามารถคลิกทะลุ overlay ได้ */
  }
  
  h1 {
    font-size: 3rem;
    font-weight: bold;
    z-index: 1;
  }
  </style>
  