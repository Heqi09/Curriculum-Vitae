<script setup>
import WelcomeItem from './WelcomeItem.vue'
import DocumentationIcon from './icons/IconDocumentation.vue'
import ToolingIcon from './icons/IconTooling.vue'
import EcosystemIcon from './icons/IconEcosystem.vue'
import CommunityIcon from './icons/IconCommunity.vue'
import SupportIcon from './icons/IconSupport.vue'

const openReadmeInEditor = () => fetch('/__open-in-editor?file=README.md')
</script>

<template>
  <section id="home" class="hero-section">
        <div class="container text-center">
          <p class="greeting">Halo, saya</p>
          <h1 class="name">Akhsanul Haq Muljadi</h1>
          <h3 class="role">Mahasiswa Teknik Informatika di Universitas Trunojoyo Madura</h3>
          <p class="short-desc">
            yang antusias dalam pengembangan web, analisis data, dan eksplorasi teknologi baru.
          </p>
        </div>
      </section>
</template>
