<template>
  <header class="navbar">
    <div class="container">
      <div class="logo">Portofolio</div>
      <nav class="menu">
        <a href="#about">Tentang</a>
        <a href="#skills">Keahlian</a>
        <a href="#projects">Proyek</a>
        <a href="#contact">Kontak</a>
      </nav>
    </div>
  </header>
</template>

<style scoped>
.navbar {
  background-color: white;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
  position: sticky;
  top: 0;
  z-index: 1000;
  padding: 1rem 0;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  font-weight: bold;
  font-size: 1.5rem;
  color: #16a34a; /* warna hijau */
}

.menu a {
  margin-left: 2rem;
  text-decoration: none;
  color: #333;
  font-weight: 500;
  position: relative;
}

.menu a:hover,
.menu a.active {
  color: #16a34a;
}

.menu a.active::after {
  content: '';
  display: block;
  width: 60%;
  margin: 0 auto;
  border-bottom: 2px solid #facc15; /* kuning */
  position: absolute;
  bottom: -6px;
  left: 0;
  right: 0;
}
</style>
