<template>
  <v-stepper v-model="e1">
    <v-stepper-header>
      <v-stepper-step :complete="e1 > 1" step="1"><h1>Choose Your Base</h1></v-stepper-step>

      <v-divider></v-divider>

      <v-stepper-step :complete="e1 >    2" step="2"><h1>Choose Fillings</h1></v-stepper-step>

      <v-divider></v-divider>

      <v-stepper-step step="3"><h1>Choose Topings</h1></v-stepper-step>
    </v-stepper-header>

    <v-stepper-items>
      <v-stepper-content step="1">
        <v-card > 
            <div v-for="(dough,i) in this.donuts.dough" v-bind:key="i" id="fill">
            <v-btn @click="total(i)"> {{ dough.name }}  </v-btn>
            <!-- <img v-for="image in images" v-bind:key="image" :src="dough.image"> -->
            </div>
        </v-card>
     <div>
         <h1>total: {{ price }} €</h1>
     </div>
        <v-btn
          color="primary"
          @click="e1 = 2">
          next step
        </v-btn>

        <v-btn flat @click="reset">Cancel</v-btn>
      </v-stepper-content>

      <v-stepper-content step="2">
          <v-card > <div v-for="(filling,i) in fillings" v-bind:key="i" id="fill" @click="outpout">
        <v-btn @click="total(i)"> {{ filling.name }}  </v-btn>
            </div>
        <img id="filling" src="http://jupiterdonuts.com/assets/images/donuts/filled-blueberry.png" alt="">
            </v-card>
     <div>
         <h1>total: {{ price }} €</h1>
     </div>
        <v-btn
          color="primary"
          @click="e1 = 3">
    
          next step
        </v-btn>

        <v-btn flat @click="reset">Cancel</v-btn>
      </v-stepper-content>

      <v-stepper-content step="3">
       <v-card>
            <div v-for="(ingridient,i) in ingridients" v-bind:key="i" id="topings" @click="outpout">
        <v-btn @click="total(i)"> {{ ingridient.name }}  </v-btn>
        <img id="topings" src="https://static1.squarespace.com/static/56d8a4ed04426221d4b69175/5b454b0588251b2395abd77f/5b454b05758d461d370a4c6b/1531269610591/BlueberryFilled.PNG" alt="">
        </div>
        </v-card>

     <div>
         <h1>total: {{ price }} €</h1>
     </div>
        <v-btn
          color="success"
          @click="buy" >
          BUY
        </v-btn>

        <v-btn flat @click="reset">Cancel</v-btn>
      </v-stepper-content>
    </v-stepper-items>
  </v-stepper>
</template>


<script>
import axios from 'axios';

export default {
    name: "Order",
    data() {
        return {
            e1: 0,
            urlApi: "https://api.myjson.com/bins/hn9xb",
            price: 0,
            donuts: []
        }
    },
    mounted() {
      axios.get(this.urlApi).then(response => {
              this.donuts = response.data;
      })
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
        },
        buy: function() {
            this.e1 = 1;
            this.price = 0;

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
    margin-bottom: 100px;
}

}

div#fill {
    display: inline-block;
.v-btn {
    margin-bottom: 400px;
    text-align: center;
    background-color: #FD8682;
    color: #fff;
}
}
div#topings {    
    display: inline-block;
.v-btn {
    margin-bottom: 400px;
    text-align: center;
    background-color: #FD8682;
    color: #fff;
    }
}
div {
    text-align: center;

}
span.primary {
    background-color: #FD8682 !important;
}
.v-card {
    
    img#dought {
     height: 300px;
    position: absolute;
    left: 42%;
     top: 15%
     }
    img#filling {
     height: 300px;
    position: absolute;
    left: 40%;
     top: 15%
     }
    
    img#topings {
     height: 300px;
    position: absolute;
    left: 40%;
     top: 15%;
     padding: 20px;
     }
    
}
</style>
