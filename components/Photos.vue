<template>
  <div class="car">
    <div>
      <b-carousel
        id="carousel-fade"
        style="text-shadow: 0px 0px 2px #000; max-width: 20rem"
        fade
        indicators
        img-width="1000"
        img-height="100"
      >
        <b-carousel-slide
          :key="item.key"
          v-for="item in db"
          :caption="item.text"
          :img-src="item.img"
        ></b-carousel-slide>
      </b-carousel>
    </div>
  </div>
</template>

<script>
export default {
  name: 'photos',
  data: () => {
    return {
      db: [
        {
          key: 0,
          text: 'Oranges',
          img: require('../images/blog1.jpg'),
          size: 20,
        },
        {
          key: 1,
          text: 'Shakes',
          img: require('../images/blog2.jpg'),
          size: 20,
        },
        {
          key: 2,
          text: 'Berries',
          img: require('../images/blog3.jpg'),
          size: 20,
        },
      ],
    }
  },
}
</script>

<style></style>
