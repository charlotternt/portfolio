<template>
  <div class="container">
    <h2>Mes projets</h2>
    <div class="projects">
      <div class="project" v-for="project in projects" :key="project.title">
        <a :href="project.url" target="_blank">
          <div class="overlay">
            <img :src="project.image" :alt="project.alt" class="picture" />
            <div class="text">{{ project.title }}</div>
          </div>
        </a>
        <div class="project-details">
          <h2>{{ project.title }}</h2>
          <p class="project-tech">{{ project.tech }}</p>
          <p>{{ project.description }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import movieImg from "../assets/movie.png";
import quizzImg from "../assets/quizz.png";
import weatherImg from "../assets/weather.png";
import calculatorImg from "../assets/calculator.png";
import ecommerceImg from "../assets/ecommerce.png";
import tictactoeImg from "../assets/tictactoe.png";

const name = "ProjectList";

const projects = [
  {
    title: "Movie",
    tech: "Vue.js",
    description: "Site affichant les sorties de films via l'API TMDB",
    url: "https://movieapitmbd.netlify.app",
    image: movieImg,
    alt: "movie",
  },
  {
    title: "Quizz",
    tech: "Vue.js",
    description: "Site d'un quizz avec Open Trivia Database",
    url: "https://quizopentriviadatabase.netlify.app",
    image: quizzImg,
    alt: "quizz",
  },
  {
    title: "Weather App",
    tech: "Vue.js • CSS",
    description: "Site affichant la météo par recherche de ville",
    url: "https://effervescent-kangaroo-6c4cd4.netlify.app",
    image: weatherImg,
    alt: "weather app",
  },
  {
    title: "Age Calculator",
    tech: "HTML • CSS • JS",
    description: "Challenge Frontend Mentor : calculateur d'âge",
    url: "https://challenge-age-calculator.netlify.app",
    image: calculatorImg,
    alt: "calculator app",
  },
  {
    title: "Product list with card",
    tech: "HTML • CSS • JS",
    description: "Challenge Frontend Mentor : site de commande de desserts.",
    url: "https://challenge-product-items.netlify.app",
    image: ecommerceImg,
    alt: "ecommerce",
  },
  {
    title: "Tic Tac Toe",
    tech: "Vue.js • CSS",
    description: "Jeu Tic Tac Toe avec un mode contre une IA",
    url: "https://tictactoeinvuejs.netlify.app",
    image: tictactoeImg,
    alt: "Tic Tac Toe",
  },
];
</script>

<style scoped>
.container {
  padding: 80px 20px;
}

.projects {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 40px;
  margin-top: 50px;
  justify-items: center;
}

.project {
  display: flex;
  flex-direction: column;
  align-items: center;
  max-width: 350px;
  width: 100%;
}

.picture {
  width: 100%;
  height: auto;
  border-radius: 5%;
  transition: 0.3s ease;
}

.overlay {
  position: relative;
  width: 100%;
  aspect-ratio: 16 / 10;
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
  z-index: 1;
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

@media (min-width: 1100px) {
  .projects {
    grid-template-columns: repeat(3, 1fr);
  }
}
</style>
