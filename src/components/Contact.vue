<template>
  <section id="contact" class="contact-section">
    <h2>Hubungi Saya</h2>
    <div class="contact-container">
      <form class="contact-form">
        <div class="form-group">
          <label for="name">Nama</label>
          <input type="text" id="name" v-model="form.name" required>
        </div>
        <div class="form-group">
          <label for="email">Email</label>
          <input type="email" id="email" v-model="form.email" required>
        </div>
        <div class="form-group">
          <label for="message">Pesan</label>
          <textarea id="message" v-model="form.message" required></textarea>
        </div>
        <button type="submit" class="submit-btn">Kirim Pesan</button>
      </form>
      <div class="contact-info">
        <h3>Informasi Kontak</h3>
        <p><i class="fas fa-envelope"></i> bagushabibi@student.uir.ac.id</p>
        <p><i class="fas fa-phone"></i> +62 822 3344 5566</p>
        <div class="social-links">
        <a href="https://linkedin.com/in/username-anda" target="_blank"><i class="fab fa-linkedin"></i></a>
        <a href="https://github.com/Bagushabibi12" target="_blank"><i class="fab fa-github"></i></a>
        <a href="https://www.instagram.com/bgusbibi_/" target="_blank"><i class="fab fa-instagram"></i></a>
        <a href="https://twitter.com/username-anda" target="_blank"><i class="fab fa-twitter"></i></a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Contact',
  data() {
    return {
      form: {
        name: '',
        email: '',
        message: ''
      }
    }
  },
  methods: {
    submitForm() {
      // Logic untuk mengirim form
      console.log('Form submitted:', this.form)
      // Reset form
      this.form = {
        name: '',
        email: '',
        message: ''
      }
    }
  }
}
</script>

<style scoped>
.contact-section {
  background-color: var(--primary);
  color: white;
}

.contact-section h2 {
  text-align: center;
  font-size: 2.5rem;
  margin-bottom: 3rem;
}

.contact-container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 3rem;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

.contact-form {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.form-group {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

.form-group label {
  font-weight: 500;
}

.form-group input,
.form-group textarea {
  padding: 0.8rem;
  border: none;
  border-radius: 4px;
  font-family: inherit;
}

.form-group textarea {
  min-height: 150px;
  resize: vertical;
}

.submit-btn {
  padding: 1rem;
  background-color: var(--accent);
  color: var(--dark);
  border: none;
  border-radius: 4px;
  font-weight: bold;
  cursor: pointer;
  transition: background-color 0.3s;
}

.submit-btn:hover {
  background-color: #ffd700;
}

.contact-info {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.contact-info h3 {
  font-size: 1.5rem;
  margin-bottom: 1rem;
}

.contact-info p {
  display: flex;
  align-items: center;
  gap: 1rem;
}

.social-links {
  display: flex;
  gap: 1.5rem;
  margin-top: 1rem;
}

.social-links a {
  color: white;
  font-size: 1.5rem;
  transition: color 0.3s;
}

.social-links a:hover {
  color: var(--accent);
}

@media (max-width: 768px) {
  .contact-container {
    grid-template-columns: 1fr;
  }
}
</style>