<template>
    <div> 
        <div class="header">
        <div id="logo">
        <router-link to="/">
        <img src="https://cdn.pixabay.com/photo/2017/11/22/16/05/pug-2970827_960_720.png" alt="">            
        </router-link>
        </div>
    <div class="nav">
        <router-link to="/Menu" class="pages">Menu</router-link>
        <router-link to="/Order" class="pages">Order</router-link>
        <router-link to="/Contact" class="pages">Contact</router-link>
    </div>
    </div>
    </div>
</template>


<style lang="scss">
body {
    margin: 0;

div#logo img {
  width: 80px; 
  margin: 5px;
}

.header {
    background-color: #fff;

}
div#logo {
  text-align: center;
  

}
.nav {
    border-bottom: 2px solid #FD8682;
    box-shadow: 0 1em 2em -1em #FD8682;
  padding-bottom: 10px;
  margin: 0;    
  list-style-type: none;
  text-align: center;

.pages {
    display: inline-block;
    padding: 0 10px;
    font-size: 16px;
    }

a {
    color: #FD8782;
    text-decoration: none;
}
}
}
</style>
