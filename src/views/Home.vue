<template>
  <div>
      <v-carousel>
      <v-carousel-item
        v-for="(item,i) in items"
        :key="i"
        :src="item.src"
      ></v-carousel-item>
    </v-carousel>
    <div id="buy">
    <router-link to="/Order.vue">
      <v-btn>ORDER NOW!!!</v-btn>
    </router-link>
    </div>
    
  </div>
</template>


<style lang="scss">
.v-carousel {
  width: 80%;
  margin: 0 auto;
  margin-top: 40px;
  height: 700px !important;
.v-window__container, .v-image {
  height: 700px !important;
}
}
div#buy {
  padding: 30px;
  // background-color: rgb(194, 223, 197);
  text-align: center;
  .v-btn {
    background-color: #D4F5F5;
    position: absolute;
    width: 200px;
    height: 60px;
    top: 65%;
    left: 45%;
  }
}

</style>

<script>
  export default {
    data () {
      return {
        items: [
          {
            src: 'https://assets.epicurious.com/photos/5ae74741f8542520401e0da6/2:1/w_1260%2Ch_630/giant-donut-cake-recipe-042718.jpg'
          },
          {
            src: 'https://donutbar.com/wp-content/uploads/2017/06/donut-bar-homers.png'
          },
          {
            src: 'https://mercatofoods.com/wp-content/uploads/2018/01/ddc27dfc-3459-4552-817e-eb2f12078a29.jpg'
          },
          {
            src: 'https://www.pngkey.com/png/full/8-89387_image-doughnuts0987650-doughnuts-wiki-anime-donut-png.png'
          }
        ]
      }
    }
  }
</script>
