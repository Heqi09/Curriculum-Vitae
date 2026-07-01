<template>
  <div class="container">
    <h2>Daftar Proyek & Dokumentasi</h2>
    
    <div v-for="proj in projects" :key="proj.id" class="project-detail">
      <h3>{{ proj.name }}</h3>
      <div class="content-grid">
        
        <div class="screenshot-wrapper">
          <img 
            v-for="(img, index) in proj.images" 
            :key="index"
            :src="getImgUrl(img)" 
            :alt="proj.name"
            class="project-img"
          />
        </div>

        <div class="tech-info">
          <p><strong>Deskripsi:</strong> {{ proj.desc }}</p>
          <p><strong>Tech Stack:</strong> {{ proj.stack }}</p>
        </div>
      </div>
    </div>
  </div>
</template>


<script setup>
const getImgUrl = (imgName) => {
  return new URL(`../assets/${imgName}`, import.meta.url).href
}

const projects = [
    {
        id: 1,
        name: 'Web Toefl Sederhana',
        desc: 'Sebuah aplikasi web sederhana untuk latihan TOEFL, menampilkan profil, riwayat pengguna, soal, hasil serta sertifikat pengguna setelah mengerjakan TOEFL.',
        stack: 'HTML, CSS, JavaScript, JSON',
        images: ['toefl.png', 'toefl2.png']
    },
    {
        id: 2,
        name: 'Sistem Kasir Bengkel Sederhana',
        desc: 'Sebuah sistem kasir sederhana untuk bengkel, dengan fitur pencatatan transaksi dan manajemen stok.',
        stack: 'HTML, CSS, PHP, MySQL',
        images: ['bengkel1.png', 'bengkel.png']
    },
    {
        id: 3,
        name: 'Web Perpustakaan',
        desc: 'Sebuah aplikasi web perpustakaan, memungkinkan pemustaka untuk melihat katalog buku, meminjam, dan mengembalikan buku. Lalu juga terdapat fitur admin untuk mengelola buku dan pemustaka.',
        stack: 'HTML, CSS, PHP, MySQL',
        images: ['perpus.png', 'perpus1.png']
    },
    {
        id: 4,
        name: 'Sistem Pemesanan Dine-In Pada Coffee Shop KOPDES',
        desc: 'Sebuah sistem pemesanan dine-in untuk coffee shop KOPDES, dengan fitur manajemen menu, pesanan, dan pembayaran.',
        stack: 'HTML, CSS, PHP, MySQL',
        images: ['kopdes.png', 'kopdes1.png']
    }
]
</script>

<style scoped>
.screenshot-wrapper {
    display: flex;
    flex-direction: column;
    gap: 1rem; 
}

h3 {
    margin-top: 2rem ;
    margin-bottom: 1rem;
    color: hsla(160, 100%, 37%, 1);
}

.project-img {
    width: 100%;
    border-radius: 8px;
    box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    object-fit: cover;
}

.content-grid { 
    display: grid; 
    grid-template-columns: 1fr 1fr; 
    gap: 2rem; 
}

@media (max-width: 768px) {
    .content-grid { grid-template-columns: 1fr; }
}
<template>
  <div class="container">
    <h2>Daftar Proyek & Dokumentasi</h2>
    
    <div v-for="proj in projects" :key="proj.id" class="project-detail">
      <h3>{{ proj.name }}</h3>
      <div class="content-grid">
        
        <div class="screenshot-wrapper">
          <img 
            v-for="(img, index) in proj.images" 
            :key="index"
            :src="getImgUrl(img)" 
            :alt="proj.name"
            class="project-img"
          />
        </div>

        <div class="tech-info">
          <p><strong>Deskripsi:</strong> {{ proj.desc }}</p>
          <p><strong>Tech Stack:</strong> {{ proj.stack }}</p>
        </div>
      </div>
    </div>
  </div>
</template>


<script setup>
const getImgUrl = (imgName) => {
  return new URL(`../assets/${imgName}`, import.meta.url).href
}

const projects = [
    {
        id: 1,
        name: 'Web Toefl Sederhana',
        desc: 'Sebuah aplikasi web sederhana untuk latihan TOEFL, menampilkan profil, riwayat pengguna, soal, hasil serta sertifikat pengguna setelah mengerjakan TOEFL.',
        stack: 'HTML, CSS, JavaScript, JSON',
        images: ['toefl.png', 'toefl2.png']
    },
    {
        id: 2,
        name: 'Sistem Kasir Bengkel Sederhana',
        desc: 'Sebuah sistem kasir sederhana untuk bengkel, dengan fitur pencatatan transaksi dan manajemen stok.',
        stack: 'HTML, CSS, PHP, MySQL',
        images: ['bengkel1.png', 'bengkel.png']
    },
    {
        id: 3,
        name: 'Web Perpustakaan',
        desc: 'Sebuah aplikasi web perpustakaan, memungkinkan pemustaka untuk melihat katalog buku, meminjam, dan mengembalikan buku. Lalu juga terdapat fitur admin untuk mengelola buku dan pemustaka.',
        stack: 'HTML, CSS, PHP, MySQL',
        images: ['perpus.png', 'perpus1.png']
    },
    {
        id: 4,
        name: 'Sistem Pemesanan Dine-In Pada Coffee Shop KOPDES',
        desc: 'Sebuah sistem pemesanan dine-in untuk coffee shop KOPDES, dengan fitur manajemen menu, pesanan, dan pembayaran.',
        stack: 'HTML, CSS, PHP, MySQL',
        images: ['kopdes.png', 'kopdes1.png']
    }
]
</script>

<style scoped>
.screenshot-wrapper {
    display: flex;
    flex-direction: column;
    gap: 1rem; 
}

h3 {
    margin-top: 2rem ;
    margin-bottom: 1rem;
    color: hsla(160, 100%, 37%, 1);
}

.project-img {
    width: 100%;
    border-radius: 8px;
    box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    object-fit: cover;
}

.content-grid { 
    display: grid; 
    grid-template-columns: 1fr 1fr; 
    gap: 2rem; 
}

@media (max-width: 768px) {
    .content-grid { grid-template-columns: 1fr; }
}
</style>