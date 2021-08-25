<template>
  <div>
    <div class="info2">
      <div class="body">
        <div class="ready2">
          <h2 class="ready1">We are ready to serve</h2>
          <h3 class="ready">
            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Rem,
            reprehenderit. <br />
          </h3>
          <h3 class="ready">
            Lorem ipsum dolor sit amet consectetur adipisicing elit Iure itaque
            unde <br />
            officia blanditiis doloribus soluta.
          </h3>
          <div class="btn-container">
            <button class="about-btn">
              <nuxt-link class="about-link" to="about">About us</nuxt-link>
            </button>
          </div>
        </div>
      </div>
    </div>
    <div>
      <Values />
    </div>
  </div>
</template>

<script>
export default {
  name: 'Info2',
}
</script>

<style scoped>
.values {
  display: flex;
  justify-content: center;
}
.info2 {
  background-image: url('../images/bg2.jpg');
  background-position: bottom;
  padding-bottom: 30px;
}
.body {
  display: flex;
  justify-content: center;
}
.ready1 {
  color: white;
  font-weight: bolder;
  display: flex;
  justify-content: center;
}
.ready {
  font-size: 20px;
  color: white;
}
.ready2 {
  display: flex;
  flex-direction: column;
}
.about-btn {
  padding: 0px;
  border-radius: 10px;
  padding: 10px;
  background: yellow;
  border-style: none;
}
.about-link {
  color: purple;
  font-size: 18px;
}
.about-link :hover {
  text-decoration: underline;
}
.btn-container {
  display: flex;
  justify-content: center;
}
</style>
