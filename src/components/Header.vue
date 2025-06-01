<template>
  <header class="header-section">
    <div class="header-container">
      <div class="header-text">
        <h1>Bagus Habibi</h1>
        <h2 class="title">Pengembang & Creator Digital</h2>
        <p class="tagline">Membantu bisnis Anda tumbuh dengan solusi digital kreatif</p>
        
        <div class="contact-section">
          <h3>Hubungi Saya</h3>
          <div class="contact-links">
            <a href="mailto:bagus@example.com" class="contact-item">
              <i class="fas fa-envelope"></i> bagushabibi@student.uir.ac.id
            </a>
            <a href="tel:+628123456789" class="contact-item">
              <i class="fas fa-phone"></i> +62 822 3344 5566
            </a>
          </div>
        </div>
      </div>

      <div class="header-image">
        <img src="../assets/images/sss.jpg" alt="Bagus Habibi" class="profile-photo">
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'HeaderSection'
}
</script>

<style scoped>
.header-section {
  min-height: 100vh;
  display: flex;
  align-items: center;
  padding: 2rem;
  background: linear-gradient(135deg, #f5f7fa 0%, #e4e8eb 100%);
}

.header-container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  max-width: 1200px;
  margin: 0 auto;
  width: 100%;
  gap: 3rem;
}

.header-text {
  flex: 1;
}

.header-text h1 {
  font-size: 3.5rem;
  color: #2c3e50;
  margin-bottom: 1rem;
  line-height: 1.2;
}

.title {
  font-size: 1.8rem;
  color: #42b983;
  margin-bottom: 1.5rem;
  font-weight: 500;
}

.tagline {
  font-size: 1.2rem;
  color: #555;
  margin-bottom: 3rem;
  max-width: 600px;
  line-height: 1.6;
}

.contact-section {
  margin-top: 3rem;
}

.contact-section h3 {
  font-size: 1.5rem;
  color: #2c3e50;
  margin-bottom: 1.5rem;
  position: relative;
  display: inline-block;
}

.contact-section h3::after {
  content: '';
  position: absolute;
  bottom: -8px;
  left: 0;
  width: 60%;
  height: 3px;
  background-color: #ffc107;
}

.contact-links {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.contact-item {
  display: flex;
  align-items: center;
  gap: 1rem;
  color: #2c3e50;
  text-decoration: none;
  font-size: 1.1rem;
  transition: color 0.3s;
}

.contact-item:hover {
  color: #42b983;
}

.contact-item i {
  font-size: 1.3rem;
  color: #ffc107;
}

.header-image {
  flex: 1;
  display: flex;
  justify-content: center;
}

.profile-photo {
  width: 100%;
  max-width: 400px;
  border-radius: 20px;
  box-shadow: 0 15px 30px rgba(0,0,0,0.1);
  transform: perspective(1000px) rotateY(-10deg);
  transition: transform 0.5s;
}

.profile-photo:hover {
  transform: perspective(1000px) rotateY(0deg);
}

@media (max-width: 992px) {
  .header-container {
    flex-direction: column-reverse;
    text-align: center;
  }

  .header-text h1 {
    font-size: 2.8rem;
  }

  .title {
    font-size: 1.5rem;
  }

  .tagline {
    margin-left: auto;
    margin-right: auto;
  }

  .contact-section h3::after {
    left: 50%;
    transform: translateX(-50%);
    width: 40%;
  }

  .contact-links {
    align-items: center;
  }
}
</style>