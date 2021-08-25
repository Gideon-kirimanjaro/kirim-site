<template>
  <div>
    <div class="items-main">
      <Navbar></Navbar>
      <b-breadcrumb class="crumb" :items="tags"></b-breadcrumb>
      <div class="sort-container">
        <b-btn variant="primary" class="mx-4" @click="sortTitleAz()"
          >sort order z-a </b-btn
        ><b-btn variant="primary" class="mx-4" @click="sortTitleZa()"
          >sort order a-z
        </b-btn>
        <b-btn variant="primary" class="mx-4" @click="sortHl()"
          >sort price high-low
        </b-btn>
        <b-btn variant="primary" class="mx-3 P-2" @click="sortLh()"
          >sort price low-high
        </b-btn>
      </div>
      <div class="clear-search">
        <b-input
          class="w-25"
          type="text"
          v-model="search"
          placeholder="...search product"
        ></b-input>
      </div>
      <b-modal id="modal-1" title="product">
        <p class="my-4">
          <a
            target="_blank"
            href="//api.whatsapp.com/send?phone=254707000574&text=Hi%20how%20are you?"
          >
            Buy via whatsapp</a
          >
        </p>
      </b-modal>

      <b-row class="ml-5 pl-5">
        <b-card
          :key="item.key"
          v-for="item in filteredItems"
          :title="item.text"
          :img-src="item.image"
          img-alt="Image"
          img-top
          tag="article"
          style="max-width: 15rem; margin-left: 20px"
          class="mb-2 mx-4"
        >
          <b-card-text>
            {{ item.text }}
          </b-card-text>
          <b-card-text>
            <h5 class="prices">kes. {{ item.price }}</h5></b-card-text
          >

          <b-button v-b-modal.modal-1 variant="warning">Buy</b-button>
        </b-card>
        <h1 v-if="toggle">Product not found!!</h1>
      </b-row>
    </div>
    <Footer />
  </div>
</template>

<script>
import Navbar from '../Navbar'
export default {
  name: 'Items',
  computed: {
    filteredItems: function () {
      return this.items.filter((value) => {
        return value.title.match(this.search.toUpperCase())
      })
    },
  },
  data: () => {
    return {
      select: '',
      search: '',
      toggle: false,
      tags: [
        {
          text: 'Home',
          href: '/',
        },
        {
          text: 'Products',
          href: true,
        },
      ],
      options: [
        { value: 'LH', text: 'Low to High Price' },
        { value: 'HL', text: 'High to Low Price' },
      ],
      items: [
        {
          key: 0,
          title: 'A',
          image: require('@/images/fruit1.jpg'),
          text: 'Product A',
          price: 1000,
        },
        {
          key: 1,
          title: 'B',
          image: require('@/images/fruit2.jpg'),
          text: 'Product B',
          price: 4000,
        },
        {
          key: 2,
          title: 'C',
          image: require('@/images/fruit3.jpg'),
          text: 'Product C',
          price: 700,
        },
        {
          key: 3,
          title: 'D',
          image: require('@/images/fruit2.jpg'),
          text: 'Product D',
          price: 300,
        },
        {
          key: 4,
          title: 'E',
          image: require('@/images/fruit5.jpg'),
          text: 'Product E',
          price: 500,
        },
        {
          key: 5,
          title: 'F',
          image: require('@/images/fruit6.jpg'),
          text: 'Product F',
          price: 600,
        },
        {
          key: 6,
          title: 'G',
          image: require('@/images/fruit7.jpg'),
          text: 'Product G',
          price: 690,
        },
        {
          key: 7,
          title: 'H',
          image: require('@/images/fruit8.jpg'),
          text: 'Product H',
          price: 790,
        },
      ],
    }
  },
  methods: {
    sortTitleAz() {
      let newItems = this.items
      newItems = newItems.sort((a, b) => {
        let A = a.text
        let B = b.text
        if (A > B) {
          return -1
        } else if (A < B) {
          return 1
        } else {
          return 0
        }
      })
      console.log(newItems)
    },
    sortTitleZa() {
      let newItems = this.items
      newItems = newItems.sort((a, b) => {
        let A = a.text
        let B = b.text
        if (B > A) {
          return -1
        } else if (B < A) {
          return 1
        } else {
          return 0
        }
      })
      console.log(newItems)
    },
    sortHl() {
      let newItems = this.items
      newItems = newItems.sort((a, b) => {
        let A = a.price
        let B = b.price
        return B - A
      })
    },
    sortLh() {
      let newItems = this.items
      newItems = newItems.sort((a, b) => {
        let A = a.price
        let B = b.price
        return A - B
      })
    },
    emptyItem() {
      if ((this.filteredItems = 0)) {
        return (this.toggle = true)
      }
    },
  },
  created() {
    this.emptyItem()
  },
}
</script>

<style>
.items-main {
  background: #ffe302;
  width: 100%;
}
.crumb {
  background: #ffe302;
}
.sort-container {
  display: flex;
  justify-content: center;
  max-width: 100%;
  margin-bottom: 0%;
}
.clear-search {
  display: flex;
  justify-content: center;
  margin-top: 20px;
  margin-bottom: 10px;
}
.prices {
  color: blue;
}
</style>
