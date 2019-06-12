<template>
    <div> 
        <div class="header">
        <div id="logo">
        <router-link to="/">
        <img src="https://cdn.pixilart.com/photos/large/22d5475f140abb9.png" alt="">            
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
  width: 100px; 
}

.header {
    background-color: rgb(212, 245, 245);

}
div#logo {
  text-align: center;
  

}
.nav {
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
