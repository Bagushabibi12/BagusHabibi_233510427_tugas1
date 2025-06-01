<template>
  <section id="about" class="about-section">
    <h2>Tentang Saya</h2>
    <div class="about-content">
      <p>Halo! Saya Bagus Habibi, seorang pengembang dan kreator digital dengan passion untuk menciptakan solusi teknologi yang inovatif dan user-friendly.</p>
      <p>Saya memiliki pengalaman lebih dari 3 tahun dalam pengembangan web dan desain antarmuka pengguna. Saya selalu bersemangat untuk mempelajari teknologi baru dan menerapkannya dalam proyek-proyek saya.</p>
      <p>Di waktu luang, saya menikmati fotografi digital dan membuat konten kreatif.</p>
    </div>
  </section>
</template>

<script>
export default {
  name: 'About'
}
</script>

<style scoped>
.about-section {
  background-color: var(--light);
  color: var(--dark);
}

.about-section h2 {
  text-align: center;
  font-size: 2.5rem;
  margin-bottom: 2rem;
  color: var(--primary);
}

.about-content {
  max-width: 800px;
  margin: 0 auto;
  text-align: center;
  font-size: 1.1rem;
}

.about-content p {
  margin-bottom: 1.5rem;
}
</style>