<template>
  <div>
    <div id="buy">
    <img src="https://www.pngkey.com/png/full/8-89387_image-doughnuts0987650-doughnuts-wiki-anime-donut-png.png" alt="">   
    <router-link to="/Order.vue">
      <v-btn>ORDER NOW!!!</v-btn>
    </router-link>
    </div>
  </div>
</template>


<style lang="scss">
div#buy {
  padding: 30px;
  // background-color: rgb(194, 223, 197);
  text-align: center;
  .v-btn {
    background-color: #D4F5F5;
    position: absolute;
    width: 200px;
    height: 60px;
    top: 50%;
    left: 45%;
  }
}

</style>

<script>

  export default {
    components: {
    }
  }
</script>
