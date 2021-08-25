<template>
  <div>
    <div class="about">
      <Navbar />
      <b-breadcrumb class="bread" :items="items"></b-breadcrumb>
      <About />
    </div>
    <Footer />
  </div>
</template>

<script>
export default {
  name: 'about',
  data: () => {
    return {
      items: [
        {
          text: 'Home',
          href: '/',
        },
        {
          text: 'About',
          href: true,
        },
      ],
    }
  },
}
</script>

<style>
.about {
  background-color: #ffe302;
}
.bread {
  background-color: #ffe302;
}
</style>
