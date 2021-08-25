<template>
  <div>
    <b-navbar toggleable="lg" type="dark">
      <b-navbar-brand>
        <nuxt-link class="melon" to="/"><i>MELONS</i></nuxt-link>
      </b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <!-- Right aligned nav items -->
        <b-navbar-nav
          id="link-container"
          style="margin-right: 80px"
          class="ml-auto"
        >
          <b-nav-item>
            <h5><nuxt-link class="link1" to="/about">About</nuxt-link></h5>
          </b-nav-item>
          <b-nav-item
            ><h5>
              <nuxt-link class="link2" to="/products">Products</nuxt-link>
            </h5></b-nav-item
          >
          <b-nav-item
            ><h5>
              <nuxt-link class="link3" to="/blog">Blog</nuxt-link>
            </h5></b-nav-item
          >
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {
  name: 'navbar',
}
</script>

<style>
.link1,
.link2,
.link3 {
  color: #056608;
}
.links:hover {
  text-decoration-line: underline;
}
.title {
  color: #056608;
}
.melon {
  padding-left: 35px;
}

/* 
@media only screen and (min-width: 768px) {
  .title {
    margin-left: 10px;
  }
}


@media only screen and (min-width: 992px) {
  .title {
    margin-left: 20px;
  }
  #link-container {
    margin-right: 20px;
  }
}


@media only screen and (min-width: 1200px) {
  .title {
    margin-left: 20px;
  }
  #link-container {
    margin-right: 20px;
  }
} */
</style>
