<template>
  <div class="contact">
    <div class="header">
      <h2>Mes réseaux</h2>
      <a href="/cv.pdf" target="_blank" class="cv-link">Mon Curriculum Vitae</a>
    </div>
    <div class="contact-item">
      <a href="https://github.com/charlotternt" target="_blank"
        ><img src="../assets/github.svg" class="icon"
      /></a>
      <a href="https://github.com/charlotternt" target="_blank"
        >Github: https://github.com/charlotternt</a
      >
    </div>
    <div class="contact-item">
      <a
        href="https://www.linkedin.com/in/charlotte-renault-94b23915b/"
        target="_blank"
        ><img src="../assets/linkedin.svg" class="icon"
      /></a>
      <a
        href="https://www.linkedin.com/in/charlotte-renault-94b23915b/"
        target="_blank"
        >LinkedIn: https://www.linkedin.com/in/charlotte-renault-94b23915b/</a
      >
    </div>
    <h2>Pour me contacter</h2>
    <div class="contact-item">
      <a href="mailto:charlotterenault3@gmail.com"
        ><img src="../assets/mail.svg" class="icon"
      /></a>
      <a href="mailto:charlotterenault3@gmail.com"
        >Email: charlotterenault3@gmail.com</a
      >
    </div>
  </div>
</template>

<script>
export default {
  name: "Social_",
};
</script>

<style>
.contact {
  margin: 50px;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}

.cv-link {
  color: #fff;
  background-color: #6540ca;
  padding: 10px 20px;
  border-radius: 4px;
  text-decoration: none;
}

.cv-link:hover {
  background-color: #a67ff0;
}

.contact-item {
  display: flex;
  align-items: center;
  margin-bottom: 15px;
}

.contact-item img.icon {
  margin-right: 10px;
  width: 24px;
  height: 24px;
}

.contact-item a,
.contact-item p {
  color: black;
  text-decoration: none;
}

.contact-item a:hover {
  text-decoration: underline;
}
</style>
