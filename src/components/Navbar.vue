<script setup>
import { ref } from 'vue'

const isOpen = ref(false)

const toggleMenu = () => {
  isOpen.value = !isOpen.value
}
</script>

<template>
  <nav class="navbar">
    <!-- Logo -->
    <div class="logo">MonApp</div>

    <!-- Hamburger -->
    <div class="burger" @click="toggleMenu">
      <span :class="{ open: isOpen }"></span>
      <span :class="{ open: isOpen }"></span>
      <span :class="{ open: isOpen }"></span>
    </div>

    <!-- Links -->
    <ul :class="['links', { open: isOpen }]">
      <li @click="isOpen = false">
        <router-link to="/">Accueil</router-link>
      </li>
      <li @click="isOpen = false">
        <router-link to="/about">À propos</router-link>
      </li>
      <li @click="isOpen = false">
        <router-link to="/contact">Contact</router-link>
      </li>
    </ul>
  </nav>
</template>

<style scoped>
.navbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 16px 24px;
  background: #044aef;
  color: white;
  position: relative;
}

/* Logo */
.logo {
  font-size: 22px;
  font-weight: bold;
}

/* Burger */
.burger {
  display: none;
  flex-direction: column;
  gap: 5px;
  cursor: pointer;
}

.burger span {
  width: 25px;
  height: 3px;
  background: white;
  transition: 0.3s;
}

/* Burger animation */
.burger span.open:nth-child(1) {
  transform: rotate(45deg) translate(5px, 5px);
}
.burger span.open:nth-child(2) {
  opacity: 0;
}
.burger span.open:nth-child(3) {
  transform: rotate(-45deg) translate(6px, -6px);
}

/* Links desktop */
.links {
  display: flex;
  list-style: none;
  gap: 24px;
}

.links a {
  color: white;
  text-decoration: none;
  font-weight: 500;
}

/* Mobile */
@media (max-width: 768px) {
  .burger {
    display: flex;
  }

  .links {
    position: absolute;
    top: 64px;
    left: 0;
    width: 100%;
    background: #0f172a;
    flex-direction: column;
    align-items: center;
    gap: 16px;
    padding: 16px 0;
    display: none;
  }

  .links.open {
    display: flex;
  }
}
</style>
