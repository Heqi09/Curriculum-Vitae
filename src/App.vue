<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <div id="app">
    <nav class="nav">
      <div class="profil">
        <img alt="Vue logo" class="logo" src="@/assets/foto-diri.jpeg" width="125" height="125" />
        <div class="profil-text">
          <h1 class="profil-name">Akhsanul Haq Muljadi</h1>
          <p>Mahasiswa Teknik Informatika</p>
        </div>
      </div>
      <div class="links">
        <router-link to="/">Home</router-link>
        <router-link to="/about">About</router-link>
        <router-link to="/project">Proyek</router-link>
      </div>
    </nav>
    <main class="content">
      <router-view />
    </main>
  </div>
</template>

<style scoped>
#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  padding: 2rem;
  font-family: Arial, sans-serif;
}

header {
  line-height: 1.5;
  max-height: 100vh;
  flex-direction: column;
}

.logo {
  margin-right: 3rem;
}

.profil {
  display: block;
  margin-bottom: 3rem;
  display: flex;
  align-items: center;
}

.profil-text p {
  color:  hsla(160, 100%, 37%, 1)
}

nav {
  width: 100%;
  font-size: 16px;
  margin-top: 2rem;
  padding-bottom: 4rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}
</style>
