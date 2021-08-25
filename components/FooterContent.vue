<template>
  <div class="footer-container">
    <b-container class="">
      <b-row>
        <b-col
          ><h3 class="ml-5">Connect with us</h3>
          <b-row>
            <b-img
              width="100"
              class="p-4"
              :key="item.key"
              v-for="item in socials"
              :src="item.icon"
            ></b-img>
          </b-row> </b-col></b-row
    ></b-container>
  </div>
</template>

<script>
export default {
  name: 'FooterContent',
  data: () => {
    return {
      socials: [
        { key: 0, icon: require('../images/fb.png') },
        {
          key: 1,
          icon: require('../images/twitter.png'),
        },
        { key: 2, icon: require('../images/ig.png') },
      ],
    }
  },
}
</script>

<style>
.footer-container {
  display: flex;
  justify-content: center;
}
</style>
