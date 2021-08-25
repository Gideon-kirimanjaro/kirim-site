<template>
  <div class="products">
    <b-card
      img-top
      :key="item.key"
      v-for="item in db"
      :img-src="item.img"
      :title="item.text"
    >
      <div class="shop">
        <b-button variant="warning">
          <nuxt-link class="products-link" to="/products"
            >View Products</nuxt-link
          >
        </b-button>
      </div>
    </b-card>
  </div>
</template>

<script>
export default {
  name: 'Products',
  data: () => {
    return {
      db: [
        {
          key: 0,
          text: 'Oranges',
          img: require('../images/fruit1.jpg'),
          size: 20,
        },
        {
          key: 1,
          text: 'Shakes',
          img: require('../images/fruit2.jpg'),
          size: 20,
        },
        {
          key: 2,
          text: 'Berries',
          img: require('../images/fruit3.jpg'),
          size: 20,
        },
      ],
    }
  },
}
</script>

<style>
.products {
  background: #d3d3d3;
  padding-bottom: 30px;
}
.card {
  min-width: 20%;
  width: 20%;
  height: 93%;
  padding-left: 8px;
  padding-right: 8px;
  margin-left: 30px;
  margin-top: 20px;
  /* animation: cards 5s ease-in-out; */
}
.products-link {
  color: white;
  font-size: 18px;
}
/* @keyframes cards {
  from {
    transform: translateX(0px);
    margin-left: -100;
  }
  to {
    transform: translateX(40px);
  }
} Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {
  .card {
    width: 70%;
  }
}

/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (min-width: 600px) {
  .card {
    width: 70%;
  }
  .products {
    display: flex;
    justify-content: center;
  }
}
@media only screen and (min-width: 768px) {
  .card {
    width: 40%;
  }
  .products {
    display: flex;
    justify-content: center;
  }
}

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {
  .card {
    width: 20%;
  }
  .products {
    display: flex;
    justify-content: center;
  }
}

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {
  .products {
    display: flex;
    justify-content: center;
  }
}
</style>
