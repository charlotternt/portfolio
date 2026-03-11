<template>
  <div class="navbar">
    <a href="#home">Accueil</a>
    <a href="#stack">À propos</a>
    <a href="#about">Compétences</a>
    <a href="#projects">Réalisations</a>
    <a href="#experience">Expérience </a>
    <a href="#social">Contact</a>
  </div>
</template>

<script>
export default {
  name: "Navbar_",
};
</script>

<style>
.navbar {
  width: 100%;
  display: flex;
  justify-content: end;
  align-items: center;
  box-sizing: border-box;
  background-color: #6540ca;
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

.navbar a.router-link-active {
  background-color: rgba(255, 255, 255, 0.3);
  border-bottom: 2px solid #ffffff;
}
</style>
