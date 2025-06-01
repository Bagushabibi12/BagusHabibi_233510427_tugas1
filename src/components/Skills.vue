<template>
  <section id="skills" class="skills-section">
    <h2>Keahlian Saya</h2>
    <div class="skills-grid">
      <div v-for="skill in skills" :key="skill.name" class="skill-card">
        <div class="skill-icon">
          <i :class="skill.icon"></i>
        </div>
        <h3>{{ skill.name }}</h3>
        <p>{{ skill.description }}</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Skills',
  data() {
    return {
      skills: [
        {
          name: 'Pengembangan Web',
          description: 'Membangun aplikasi web responsif dengan Vue.js, React, dan Node.js',
          icon: 'fas fa-code'
        },
        {
          name: 'Desain UI/UX',
          description: 'Mendesain antarmuka pengguna yang intuitif dan menarik',
          icon: 'fas fa-paint-brush'
        },
        {
          name: 'Fotografi Digital',
          description: 'Membuat konten visual yang menarik untuk berbagai kebutuhan',
          icon: 'fas fa-camera'
        },
        {
          name: 'Editing Video',
          description: 'Produksi konten video kreatif untuk media sosial dan web',
          icon: 'fas fa-video'
        }
      ]
    }
  }
}
</script>

<style scoped>
.skills-section {
  background-color: white;
  color: var(--dark);
}

.skills-section h2 {
  text-align: center;
  font-size: 2.5rem;
  margin-bottom: 3rem;
  color: var(--primary);
}

.skills-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

.skill-card {
  background: var(--light);
  padding: 2rem;
  border-radius: 8px;
  text-align: center;
  transition: transform 0.3s, box-shadow 0.3s;
}

.skill-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 20px rgba(0,0,0,0.1);
}

.skill-icon {
  font-size: 2.5rem;
  color: var(--secondary);
  margin-bottom: 1.5rem;
}

.skill-card h3 {
  margin: 1rem 0;
  color: var(--primary);
}

.skill-card p {
  color: #666;
}
</style>