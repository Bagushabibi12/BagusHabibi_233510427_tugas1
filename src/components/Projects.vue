<template>
  <section id="projects" class="projects-section">
    <h2>Proyek Saya</h2>
    <div class="projects-grid">
      <div v-for="project in projects" :key="project.title" class="project-card">
        <img :src="project.image" :alt="project.title" class="project-image" />
        <div class="project-info">
          <h3>{{ project.title }}</h3>
          <p>{{ project.description }}</p>
          <a :href="project.link" class="project-link">Lihat Proyek</a>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import brandImage from '../assets/images/brand-umkm.jpg'
import feedImage from '../assets/images/instagram-feed.jpg'
import assetsImage from '../assets/images/digital-assets.jpg'

export default {
  name: 'Projects',
  data() {
    return {
      projects: [
        {
          title: 'Brand Identity untuk UMKM',
          description:
            'Merancang logo, palet warna, dan elemen visual untuk brand lokal agar tampil profesional dan konsisten.',
          image: brandImage,
          link: '#'
        },
        {
          title: 'Desain Feed Instagram Kreatif',
          description:
            'Koleksi konten visual untuk sosial media dengan pendekatan estetika dan storytelling yang kuat.',
          image: feedImage,
          link: '#'
        },
        {
          title: 'Digital Asset Kit untuk Creator',
          description:
            'Set aset digital seperti icon pack, template konten, dan elemen grafis untuk menunjang personal branding.',
          image: assetsImage,
          link: '#'
        }
      ]
    }
  }
}
</script>

<style scoped>
.projects-section {
  background-color: var(--light);
  color: var(--dark);
}

.projects-section h2 {
  text-align: center;
  font-size: 2.5rem;
  margin-bottom: 3rem;
  color: var(--primary);
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
}

.project-card {
  background: white;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s;
}

.project-card:hover {
  transform: translateY(-5px);
}

.project-image {
  width: 100%;
  height: 200px;
  object-fit: cover;
}

.project-info {
  padding: 1.5rem;
}

.project-info h3 {
  margin: 0 0 1rem;
  color: var(--primary);
}

.project-info p {
  color: #666;
  margin-bottom: 1.5rem;
}

.project-link {
  display: inline-block;
  padding: 0.5rem 1rem;
  background-color: var(--secondary);
  color: white;
  text-decoration: none;
  border-radius: 4px;
  transition: background-color 0.3s;
}

.project-link:hover {
  background-color: var(--primary);
}
</style>
