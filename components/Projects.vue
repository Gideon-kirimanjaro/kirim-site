<template>
  <div>
    <h1 ref="header" class="header">PROJECTS</h1>
    <div class="projects-container">
      <div class="linksS" :key="item" v-for="item of db">
        <a target="_blank" href="https://kirim-gbv.netlify.app/">
          <img class="project-img" width="250" height="200" :src="item.image" />
          <h3 class="header">
            {{ item.titles }}
          </h3>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
import Carousel from './ÙI/Carousel'
export default {
  name: 'Projects',
  data: () => {
    return {
      db: [
        { titles: 'GBV Web App', image: require('../images/pic2.jpg') },
        { titles: 'Sign up/Sign In', image: require('../images/pic3.jpg') },
        { titles: 'BRC', image: require('../images/pic3.jpg') },
        { titles: 'BRC', image: require('../images/pic2.jpg') },
        { titles: 'BRC', image: require('../images/pic2.jpg') },
        { titles: 'BRC', image: require('../images/pic2.jpg') },
      ],
    }
  },
}
</script>

<style>
.header {
  color: white;
  margin-left: 80px;
}
.projects-container {
  margin-left: 100px;

  margin-bottom: 100px;
  margin-top: 20px;
  display: flex;
  flex-wrap: wrap;
}
a {
  text-decoration: none;
}
a:hover {
  text-decoration: underline;
  color: yellow;
}
.project-img:hover {
  animation: x 2s ease-in-out;
}
.linksS {
  display: flex;
  flex-wrap: wrap;
  margin-right: 100px;
  margin-bottom: 30px;
}
@keyframes x {
  0% {
    transform: scale(1);
  }
  100% {
    transform: scale(1.1);
  }
}
@media only screen and (max-width: 600px) {
  .projects-container {
    margin-left: 50px;
  }
}
@media only screen and (max-width: 653px) and (min-width: 280px) {
  .projects-container {
    margin-left: 40px;
  }
}
@media only screen and (max-width: 1024px) and (min-width: 768px) {
  .projects-container {
    margin-left: 15px;
  }
}
@media only screen and (max-width: 1366px) and (min-width: 1024px) {
  .projects-container {
    margin-left: 80px;
  }
}
</style>
