
<template>
<div>
        <div v-for="(ingridient,i) in ingridients" v-bind:key="i">
        <v-btn @click="total(i)"> {{ ingridient.name }}  </v-btn>
     </div>

     <div>
         <h1>{{ price }} €</h1>
     </div>
</div>
</template>









<script>
export default {
    name: "Order",
    data() {
        return {
            price: 0,
            ingridients: [
                {
                    name: "Milk Chocolate",
                    price: 0.50
                },
                {
                    name: "White Chocolate",
                    price: 0.50
                },
                {
                    name: "Dark Chocolate",
                    price: 0.60
                },
                {
                    name: "Strawberries",
                    price: 0.70
                },
                {
                    name: "Caramel",
                    price: 0.30
                },
            ]
        }
    },
    methods: {
        total: function(a) {
            this.price += this.ingridients[a].price;
            
        }
    }
}
</script>


<style lang="scss">
.v-btn {
    display: inline;
}
</style>
