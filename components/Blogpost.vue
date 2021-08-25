<template>
  <div class="blog">
    <Navbar />
    <b-breadcrumb class="crumb-blog" :items="tags"></b-breadcrumb>
    <div class="frame">
      <iframe
        width="824"
        height="860"
        src="https://app.powerbi.com/view?r=eyJrIjoiYjU4MTE0NWItNGM1ZC00YTYzLTkwZmItY2ZlOWE1ZjkzOWFjIiwidCI6IjJkYzk0ZDczLWE4ZWMtNGRjYS04NGEwLTBjZjRmMjdmOTVkOCJ9"
        frameborder="0"
        allowFullScreen="true"
      ></iframe>
    </div>
    <div class="hero">
      <b-row>
        <b-col>
          <div class="car"><Photos /></div> </b-col
      ></b-row>
    </div>
    <div class="hero2">
      <b-row>
        <b-col>
          <b-card
            style="max-width: 60rem"
            class="mb-2"
            :key="item"
            v-for="item in blogDb"
          >
            <div class="blog-img">
              <b-img class="" width="500" height="500" :src="item.img"></b-img>

              <h3 class="px-4">{{ item.header }}</h3>
              <h5 class="px-4">{{ item.content }}</h5>
            </div>
          </b-card></b-col
        ></b-row
      >
    </div>
  </div>
</template>

<script>
export default {
  name: 'Blogpost',
  data: () => {
    return {
      blogDb: [
        {
          img: require('../images/blog1.jpg'),
          header: 'The rise of the indigenous fruit',
          content:
            'Fruit and vegetables should be an important part of your daily diet. They are naturally good and contain vitamins and minerals that can help to keep you healthy. They can also help protect against some diseases.',
        },
        {
          img: require('../images/blog2.jpg'),
          header: 'The healthy lifestyle',
          content:
            'Fruit and vegetables should be an important part of your daily diet. They are naturally good and contain vitamins and minerals that can help to keep you healthy. They can also help protect against some diseases.',
        },
        {
          img: require('../images/blog3.jpg'),
          header: 'The rise of the indigenous fruit',
          content:
            'Fruit and vegetables should be an important part of your daily diet. They are naturally good and contain vitamins and minerals that can help to keep you healthy. They can also help protect against some diseases.',
        },
      ],
      tags: [
        {
          text: 'Home',
          href: '/',
        },
        {
          text: 'blog',
          href: true,
        },
      ],
    }
  },
}
</script>

<style>
.hero {
  display: flex;
  justify-content: center;
}
.hero2 {
  display: flex;
  justify-content: center;
  margin-top: 30px;
  background-color: rgb(224, 221, 221);
}
.blog {
  background-color: yellow;
}
.blog-img {
  height: 70%;
}
.crumb-blog {
  background-color: rgb(255, 255, 0);
}
.frame {
  display: flex;
  justify-content: center;
  margin-bottom: 20px;
  margin-top: 10px;
}
</style>
