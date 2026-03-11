<template>
  <div class="stack">
    <h2>Mes Compétences</h2>

    <p>
      Au cours de mes études j'ai pu découvrir et apprendre différents langages.
      Nous avions commencer par voir les bases en HTML, CSS ,PHP et Javascript
      ensuite on a du réaliser des petits projets en react, vue js ,python,
      java, ruby. Je suis plus à l'aise avec le language Vue Js.
    </p>
    <div class="images-container">
      <div class="tech">
        <img class="logo" src="../assets/html.png" />
        <span>HTML</span>
      </div>

      <div class="tech">
        <img class="logo" src="../assets/css.png" />
        <span>CSS</span>
      </div>

      <div class="tech">
        <img class="logo" src="../assets/php.png" />
        <span>PHP</span>
      </div>

      <div class="tech">
        <img class="logo" src="../assets/javascript.svg" />
        <span>JavaScript</span>
      </div>

      <div class="tech">
        <img class="logo" src="../assets/laravel.png" />
        <span>Laravel</span>
      </div>

      <div class="tech">
        <img class="logo" src="../assets/vuejs.png" />
        <span>Vue JS</span>
      </div>

      <div class="tech">
        <img class="logo" src="../assets/react.png" />
        <span>React</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "stack_",

  mounted() {
    const techs = document.querySelectorAll(".tech");

    const observer = new IntersectionObserver(
      (entries) => {
        entries.forEach((entry, index) => {
          if (entry.isIntersecting) {
            setTimeout(() => {
              entry.target.classList.add("show");
            }, index * 150);
          }
        });
      },
      { threshold: 0.3 }
    );

    techs.forEach((tech) => {
      observer.observe(tech);
    });
  },
};
</script>

<style>
.stack {
  padding: 100px 50px;
  background-color: #f5f7ff;
}

.images-container {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 30px;
  margin-top: 50px;
}

.tech {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;

  width: 120px;
  height: 120px;

  background: white;
  border-radius: 15px;

  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.08);

  opacity: 0;
  transform: translateY(40px);
  transition: all 0.6s ease;
}

.tech.show {
  opacity: 1;
  transform: translateY(0);
}

.tech img {
  width: 45px;
  height: 45px;
  margin-bottom: 10px;
}

.tech span {
  font-size: 14px;
  color: #444;
  font-weight: 500;
}

.tech:hover {
  transform: translateY(-8px);
  box-shadow: 0 12px 30px rgba(0, 0, 0, 0.15);
}
</style>
