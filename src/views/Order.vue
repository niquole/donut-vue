
<template>
<div>
    <h1>Build your dream donut from scratch!</h1>
    <h2>Choose your Filling :)</h2>
    <div v-for="(filling,i) in fillings" v-bind:key="i" id="fill">
        <v-btn @click="total(i)"> {{ filling.name }}  </v-btn>
    </div>
    <h2>Choose Ingridients</h2>
        <div v-for="(ingridient,i) in ingridients" v-bind:key="i" id="ingri">
        <v-btn @click="total(i)"> {{ ingridient.name }}  </v-btn>
     </div>
        <div @click="outpout">

        </div>
    <v-btn @click="reset" color="error" type="submit"> x </v-btn>
     <div>
         <h1>total: {{ price }} €</h1>
     </div>
     <v-btn color="success" >Buy!</v-btn>
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
            ],
            fillings: [
                {
                    name: "Plane donut",
                    price: 0.80
                },
                {
                    name: "Chocolate filling",
                    price: 1.00
                },
                {
                    name: "Caramel filling",
                    price: 0.90
                }

            ]
        }
    },
    methods: {
        total: function(a) {
            this.price += this.ingridients[a].price;
            this.price += this.fillings[a].price;

        },
        reset: function() {
            this.price = 0;
        },
        outpout: function() {
            this.ingridients.name;
            this.fillings.name;
        }
    }
}
</script>


<style lang="scss">

div#ingri{
    display: inline-block;
    text-align: center;
    
.v-btn {
    text-align: center;
    background-color: #FD8682;
    color: #fff;
}

}

div#fill {
    margin-bottom: 100px;
    display: inline-block;
.v-btn {
    text-align: center;
    background-color: #FD8682;
    color: #fff;
}
}
div {
    text-align: center;

}
</style>
