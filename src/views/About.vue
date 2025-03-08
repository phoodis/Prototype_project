<template>
    <div class="about-container">
      <div class="card">
        <img class="profile-img" src="https://source.unsplash.com/200x200/?portrait" alt="Profile Picture" />
        <h1>About Me</h1>
        <p class="name">John Doe</p>
        <p class="bio">I am a passionate software developer with expertise in Vue.js, JavaScript, and modern web technologies. I love building user-friendly applications and exploring new technologies.</p>
        <div class="social-links">
          <a href="https://github.com/" target="_blank">GitHub</a>
          <a href="https://linkedin.com/" target="_blank">LinkedIn</a>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'About'
  };
  </script>
  
  <style scoped>
 .about-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  width: 100vw; /* ให้กินพื้นที่ทั้งจอ */
  background: linear-gradient(135deg, #667eea, #764ba2);
}
  
  .card {
    background: rgba(255, 255, 255, 0.15);
    padding: 2rem;
    border-radius: 15px;
    text-align: center;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
    backdrop-filter: blur(10px);
    margin: auto;
    max-width: 500px;
  }
  
  .profile-img {
    width: 120px;
    height: 120px;
    border-radius: 50%;
    object-fit: cover;
    margin-bottom: 1rem;
    border: 3px solid white;
  }
  
  h1 {
    font-size: 2rem;
    margin-bottom: 0.5rem;
  }
  
  .name {
    font-size: 1.5rem;
    font-weight: bold;
  }
  
  .bio {
    font-size: 1rem;
    margin: 1rem 0;
    opacity: 0.9;
  }
  
  .social-links a {
    display: inline-block;
    margin: 0.5rem;
    color: white;
    text-decoration: none;
    font-weight: bold;
    transition: 0.3s;
  }
  
  .social-links a:hover {
    text-decoration: underline;
  }
  </style>
  