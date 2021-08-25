<template>
  <div>
    <div class="content">
      <div class="content2">
        <img
          class="infoImg"
          height="100"
          width="100"
          src="../images/fruits.png"
          alt=""
        />
        <h2 class="mini">Delicious & tantalizing Water Melons</h2>
        <h3 class="name">
          This is the best all-in-one place to <br />find your water melons.
          View our offers on <br />
          our products page
        </h3>
        <button class="projects">
          <b-link
            class="view1"
            @click="projectScroll('header')"
            target="_blank"
          >
            View Products
          </b-link>
        </button>
        <button class="projects2">
          <b-link class="view" target="_blank"> Contact us </b-link>
        </button>
        <h3 class="test" ref="header"></h3>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'info',
  methods: {
    projectScroll(refName) {
      var element = this.$refs[refName]
      var top = element.offsetTop

      window.scrollTo(0, top)
    },
  },
}
</script>

<style>
.name {
  color: #056608;
}
.view {
  font-size: 20px;
  color: purple;
}
.view1 {
  font-size: 20px;
  color: white;
}
.mini {
  color: #056608;
  font-weight: bolder;
  font-size: 30px;
}

.infoImg {
  display: flex;
  justify-content: center;
}
.projects {
  border-style: none;
  border-radius: 25px;
  padding: 10px;
  background-color: rgb(131, 4, 114);
  margin-top: 30px;
  animation: example 4s ease-in-out;
}
.projects:hover {
  color: yellow;
}
.projects2 {
  border-style: none;
  border-radius: 25px;
  padding: 10px;
}
.content {
  position: relative;
  display: flex;
  justify-content: center;
  margin-top: 50px;
}

.test {
  margin-top: 100px;
}
@keyframes example {
  from {
    margin-top: -150px;
  }
  to {
    margin-top: 30px;
  }
}

/* .content2 {
  display: flex;
  justify-content: ;
} */
/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
  .name {
    font-size: 20px;
  }
}

/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (min-width: 600px) {
  .projects {
    margin-left: 70px;
  }
}
/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
  .projects {
    margin-left: 40px;
  }
}

/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (min-width: 600px) {
  .projects {
    margin-left: 70px;
  }
}

/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {
  .projects {
    margin-left: 70px;
  }
}

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {
  .projects {
    margin-left: 90px;
  }
}
</style>
