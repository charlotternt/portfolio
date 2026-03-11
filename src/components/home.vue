<template>
  <div class="app">
    <h1>Bonjour,</h1>
    <h2>Je suis Charlotte</h2>
    <h3>Développeuse web junior</h3>
    <a href="#about" class="btn">Qui suis-je ?</a>
  </div>
</template>

<script>
export default {
  name: "Home_",
};
</script>

<style>
.app {
  background-image: url("../assets/background.jpeg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  background-color: rgba(0, 0, 0, 0.4);
  background-blend-mode: darken;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.btn {
  display: inline-block;
  padding: 10px 20px;
  margin: 10px;
  background-color: #6540ca;
  color: white;
  text-decoration: none;
  border-radius: 5px;
}

.btn:hover {
  background-color: #a67ff0;
}
</style>
