<template>
  <div class="navbar">
    <div class="menu-toggle" @click="toggleMenu">☰</div>

    <div class="links" :class="{ active: isOpen }">
      <a href="#home">Accueil</a>
      <a href="#stack">À propos</a>
      <a href="#about">Compétences</a>
      <a href="#projects">Réalisations</a>
      <a href="#experience">Expérience</a>
      <a href="#social">Contact</a>
    </div>
  </div>
</template>

<script>
export default {
  name: "Navbar_",
  data() {
    return {
      isOpen: false,
    };
  },
  methods: {
    toggleMenu() {
      this.isOpen = !this.isOpen;
    },
  },
};
</script>

<style>
.navbar {
  width: 100%;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  background-color: #6540ca;
  box-sizing: border-box;
  padding: 10px 20px;
}

.links {
  display: flex;
  gap: 10px;
}

.navbar a {
  color: #c9b8f5;
  font-size: 18px;
  text-decoration: none;
  font-weight: bold;
  padding: 10px;
  border-radius: 5px;
  transition: background-color 0.3s;
}

.navbar a:hover {
  background-color: rgba(255, 255, 255, 0.2);
}

.menu-toggle {
  display: none;
  font-size: 28px;
  color: #c9b8f5;
  cursor: pointer;
}

@media (max-width: 768px) {
  .menu-toggle {
    display: block;
  }

  .links {
    position: absolute;
    top: 60px;
    right: 0;
    background: #6540ca;
    flex-direction: column;
    width: 200px;
    display: none;
  }

  .links.active {
    display: flex;
  }
}
</style>
