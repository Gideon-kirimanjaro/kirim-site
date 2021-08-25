<template>
  <div class="values-main">
    <!-- <b-row class="justify-content-center"
      ><h1 class="values-header">Our Values</h1></b-row
    > --><b-row class="justify-content-center"
      ><h1 class="values-header">Our Values</h1></b-row
    >

    <b-container class="ml-5 mt-4 p-5" fluid>
      <div class="container">
        <b-row>
          <b-col
            class="mt-sm-2 pl-4"
            sm="auto"
            md="auto"
            lg="3"
            :key="item.key"
            v-for="item in valuesDb"
          >
            <b-col class="px-1 ml-4">
              <img width="100" height="100" :src="item.image" alt="pic" />
              <h4 class="values-text">{{ item.text }}</h4>
            </b-col>
            <h5>{{ item.body }}</h5>
            <hr size="8" width="100%" color="purple" /> </b-col
        ></b-row>
      </div>
    </b-container>
  </div>
</template>

<script>
export default {
  name: 'Values',
  data: () => {
    return {
      valuesDb: [
        {
          key: 0,
          image: require('../images/hand.png'),
          text: 'Commitment',
          body: 'we are commited to offering the best',
        },
        {
          key: 1,
          image: require('../images/love.png'),
          text: 'Passion',
          body: 'We are passionate to our customers',
        },
        {
          key: 2,
          image: require('../images/trust.png'),
          text: 'Trust',
          body: 'Transparency is key to our business',
        },
        {
          key: 3,
          image: require('../images/transaction.png'),
          text: 'Integrity',
          body: 'We value integrity and transparency',
        },
      ],
    }
  },
}
</script>

<style>
.values {
  display: flex;
  justify-content: center;
}
/* .values-container {
  padding: 20px;
  margin-left: 10px;
} */
.values-main {
  background: #f3f0e8;
}
.values-text {
  color: purple;
}
.values-header {
  color: purple;
}
.image-text {
  margin-left: 80px;
}
.container {
  display: flex;
  justify-content: center;
}
@media only screen and (max-width: 800px) {
  .values-header {
    margin-right: 50px;
  }
} /*
@media only screen and (max-width: 736px) {
  .container {
    margin-left: 50px;
  }
}

@media only screen and (max-width: 760px) {
  .container {
    margin-left: 70px;
  }
} */
</style>
