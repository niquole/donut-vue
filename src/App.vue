<template>
  <v-app>

      <Header/>
      <Home/>
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
import Home from './views/Home'




export default {
  name: 'App',
  components: {
    Header,
    Footer,
    Home

  },
  data () {
    return {
      //
    }
  }
}
</script>
