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
    <router-link to="/Order">
      <v-btn>ORDER NOW!</v-btn>
    </router-link>
    </div>
    
  </div>
</template>


<style lang="scss">
.v-carousel {
  width: 100%;
  margin: 0 auto;
  margin: 0;
  height: 800px !important;
.v-window__container, .v-image {
  height: 800px !important;
}
}
div#buy {
  padding: 25px;
  // background-color: rgb(194, 223, 197);
  text-align: center;
  .v-btn {
    background-color: #D4F5F5;
    position: absolute;
    width: 160px;
    height: 60px;
    top: 65%;
    left: 45%;
    margin-left: 10px;
    padding-left: 10px;
  }
}

</style>

<script>
  export default {
    data () {
      return {
        items: [
          {
            src: 'https://images2.minutemediacdn.com/image/upload/c_crop,h_1414,w_2101,x_10,y_0/v1554924835/shape/mentalfloss/88294-istock-905879330.jpg?itok=J3gVztV_'
          },
          {
            src: 'https://media.cntraveler.com/photos/59ca6488e11975084c5841ea/master/pass/Federal_160415_FEDERALdonuts64786.jpg'
          },
          {
            src: 'https://cdn.pixabay.com/photo/2017/08/11/21/46/donuts-2632878_960_720.jpg'
          },
          {
            src: 'http://www.minnesotamonthly.com/wp-content/uploads/sites/85/2018/05/gd-homepage_header-small-nologo.jpg'
          }
        ]
      }
    }
  }
</script>
