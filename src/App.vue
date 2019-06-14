<template>
  <v-app>

      <Header/>
      <router-view></router-view>
  <Footer/>
  </v-app>
</template>

<style>
#app {
  background-color: rgb(194, 223, 197);
  
}
</style>

<script>
import Header from './components/Header'
import Footer from './components/Footer'




export default {
  name: 'App',
  components: {
    Header,
    Footer

  },
  data () {
    return {
      //
    }
  }
}
</script>
