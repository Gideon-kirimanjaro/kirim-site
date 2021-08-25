<template>
  <div>
    <div class="about-container">
      <b-container fluid>
        <b-row>
          <b-col sm="auto" md="auto" lg="5">
            <b-img
              height="400"
              width="400"
              src="@/images/about.jpg"
              rounded="circle"
              alt="Circle image"
            ></b-img
          ></b-col>
          <b-col>
            <div>
              <h2 class="story">Our story</h2>
              <p>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Et
                autem cumque quaerat quasi incidunt eveniet fuga consequuntur
                rem distinctio, tempore recusandae omnis officiis magni rerum
                maxime veritatis eius quod at! Lorem ipsum, dolor sit amet
                consectetur adipisicing elit. Cupiditate accusamus repudiandae
                nostrum iste expedita laudantium, excepturi eius. Aperiam,
                inventore, quae eum dolor id debitis tempora doloremque,
                adipisci harum provident minima. Lorem ipsum dolor sit amet
                consectetur adipisicing elit. Quod dignissimos ipsa tempora
                consequatur asperiores. Possimus explicabo ratione laboriosam
                incidunt, voluptatem quae quasi. Cum vitae accusamus cupiditate
                repellat provident ipsam impedit? Lorem ipsum dolor sit amet
                consectetur adipisicing elit. Distinctio amet, iusto obcaecati
                impedit, repellendus dolores vero, velit repellat dolor fugiat a
                dolorem omnis mollitia non expedita tempora voluptatem
                voluptates autem.
              </p>
              <h2 class="story">Our Mission</h2>
              <p>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Et
                autem cumque quaerat quasi incidunt eveniet fuga consequuntur
                rem distinctio, tempore recusandae omnis officiis magni rerum
                maxime veritatis eius quod at! Lorem ipsum, dolor sit amet
                consectetur adipisicing elit. Cupiditate accusamus repudiandae
                nostrum iste expedita laudantium, excepturi eius. Aperiam,
                inventore, quae eum dolor id debitis tempora doloremque,
                adipisci harum provident minima. Lorem ipsum dolor sit amet
                consectetur adipisicing elit. Quod dignissimos ipsa tempora
                consequatur asperiores. Possimus explicabo ratione laboriosam
                incidunt, voluptatem quae quasi. Cum vitae accusamus cupiditate
                repellat provident ipsam impedit? Lorem ipsum dolor sit amet
                consectetur adipisicing elit. Distinctio amet, iusto obcaecati
                impedit, repellendus dolores vero, velit repellat dolor fugiat a
                dolorem omnis mollitia non expedita tempora voluptatem
                voluptates autem.
              </p>
              <h2 class="story">Our Vision</h2>
              <p>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Et
                autem cumque quaerat quasi incidunt eveniet fuga consequuntur
                rem distinctio, tempore recusandae omnis officiis magni rerum
                maxime veritatis eius quod at! Lorem ipsum, dolor sit amet
                consectetur adipisicing elit. Cupiditate accusamus repudiandae
                nostrum iste expedita laudantium, excepturi eius. Aperiam,
                inventore, quae eum dolor id debitis tempora doloremque,
                adipisci harum provident minima. Lorem ipsum dolor sit amet
                consectetur adipisicing elit. Quod dignissimos ipsa tempora
                consequatur asperiores. Possimus explicabo ratione laboriosam
                incidunt, voluptatem quae quasi. Cum vitae accusamus cupiditate
                repellat provident ipsam impedit? Lorem ipsum dolor sit amet
                consectetur adipisicing elit. Distinctio amet, iusto obcaecati
                impedit, repellendus dolores vero, velit repellat dolor fugiat a
                dolorem omnis mollitia non expedita tempora voluptatem
                voluptates autem.
              </p>
            </div></b-col
          ></b-row
        ></b-container
      >
    </div>
  </div>
</template>

<script>
export default {
  name: 'About',
  data: () => {
    return {
      abouts: [
        {
          header: 'Our Story',
        },
      ],
    }
  },
}
</script>

<style>
.about-container {
  padding-left: 60px;
}
.story {
  display: flex;
  justify-content: center;
  padding-top: 20px;
}
</style>
