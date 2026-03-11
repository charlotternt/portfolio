<template>
  <div class="container">
    <h2>Mes projets</h2>
    <div class="projects">
      <div class="project">
        <a
          href="https://effervescent-kangaroo-6c4cd4.netlify.app"
          target="_blank"
        >
          <div class="overlay">
            <img
              src="../assets/weather.png"
              alt="weather app"
              class="picture"
            />
            <div class="text">Weather App</div>
          </div>
        </a>
        <div class="project-details">
          <h2>Weather App</h2>
          <p class="project-tech">Vue.js • CSS</p>
          <p>Réalisation d'une page web qui donne la météo.</p>
        </div>
      </div>
      <div class="project">
        <a href="https://challenge-age-calculator.netlify.app" target="_blank">
          <div class="overlay">
            <img
              src="../assets/calculator.png"
              alt="calculator app"
              class="picture"
            />
            <div class="text">Age Calculator</div>
          </div>
        </a>
        <div class="project-details">
          <h2>Age Calculator</h2>
          <p class="project-tech">HTML • CSS • JS</p>
          <p>
            Réalisation d'une page web qui permet de calculer l'âge en fonction
            de la date de naissance.
          </p>
        </div>
      </div>
      <div class="project">
        <a href="https://challenge-product-items.netlify.app" target="_blank">
          <div class="overlay">
            <img
              src="../assets/ecommerce.png"
              alt="ecommerce"
              class="picture"
            />
            <div class="text">Commande de desserts</div>
          </div>
        </a>
        <div class="project-details">
          <h2>Commande de desserts</h2>
          <p class="project-tech">HTML • CSS • JS</p>
          <p>Réalisation d'une page web qui simule une commande de desserts.</p>
        </div>
      </div>
      <div class="project">
        <a href="https://tictactoeinvuejs.netlify.app" target="_blank">
          <div class="overlay">
            <img
              src="../assets/tictactoe.png"
              alt="Tic Tac Toe"
              class="picture"
            />
            <div class="text">Tic Tac Toe</div>
          </div>
        </a>
        <div class="project-details">
          <h2>Tic Tac Toe</h2>
          <p class="project-tech">Vue.js • CSS</p>
          <p>
            Réalisation du jeu Tic Tac Toe avec la possibilité de jouer contre
            une ia.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "project_",
};
</script>

<style>
.container {
  padding: 100px 50px;
}

.projects {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 50px;
  justify-items: center;
  margin-top: 50px;
}

.project {
  display: flex;
  flex-direction: column;
  align-items: center;
  max-width: 350px;
}

.picture {
  width: 350px;
  height: 220px;
  border-radius: 5%;
  transition: 0.3s ease;
}

.overlay {
  position: relative;
  width: 350px;
  height: 220px;
  border-radius: 5%;
  overflow: hidden;
}

.overlay::after {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.281);
  transition: 0.3s ease;
  opacity: 0;
}

.overlay:hover::after {
  opacity: 1;
}

.text {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: #6540ca;
  font-size: 20px;
  font-weight: bold;
  visibility: hidden;
  opacity: 0;
  transition: visibility 0s, opacity 0.3s ease;
}

.overlay:hover .text {
  visibility: visible;
  opacity: 1;
}

.project-details {
  text-align: center;
  margin-top: 15px;
}

.project-details h2 {
  margin-top: 0;
}

.project-details p {
  margin-top: 5px;
}

.project-tech {
  font-size: 14px;
  color: black;
  font-weight: 600;
}

@media (max-width: 768px) {
  .projects {
    grid-template-columns: 1fr;
  }
}
</style>
