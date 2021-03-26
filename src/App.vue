<template>
  <div id="app">
    <Hero v-bind:cart="cart"/>
    
    <Product v-bind:products="products" v-on:add-cart="addCart"/>
    
  </div>
</template>

<script>
import Hero from "./components/Hero";
import Product from "./components/Product";
export default {
  name: 'App',
  components: {
    Hero,
    Product,
  },
  data(){
    return{
      products: [
        {
          id: 1,
          name: 'O.Black Shirt',
          price:  3000,
          img: require('./assets/products/p1.jpg')
        },
        {
          id: 2,
          name: 'W.Blue Shirt',
          price: 2500,
          img: require('./assets/products/p2.jpg')
        },
        {
          id: 3,
          name: 'strip Shirt',
          price:  2500,
          img: require('./assets/products/p3.jpg')
        },
        {
          id: 4,
          name: 'red shirt',
          price:  1500,
          img: require('./assets/products/p4.jpeg')
        },
        {
          id: 5,
          name: 'White Mens',
          price:  3500,
          img: require('./assets/products/p5.jpeg')
        },
        {
          id: 6,
          name: 'Sexy Ladies top',
          price:  2500,
          img: require('./assets/products/p6.jpeg')
       },
        {
          id: 7,
          name: 'Mens Boot',
          price:  2500,
          img: require('./assets/products/p7.jpeg')
     },
        {
          id: 8,
          name: 'Snicks',
          price:  10000,
          img: require('./assets/products/p8.jpeg')
        },
        {
          id: 9,
          name: 'sports',
          price:  12500,
          img: require('./assets/products/p9.jpeg')
        },
        {
          id: 10,
          name: 'LSM',
          price:  5500,
          img: require('./assets/products/p10.jpeg')
        },
        {
          id: 11,
          name: 'Timber Land Women',
          price:  22500,
          img: require('./assets/products/p11.jpeg')
        },
        {
          id: 12,
          name: 'Red Shoes',
          price:  5000,
          img: require('./assets/products/p12.jpeg')        },
        {
          id: 13,
          name: 'Brown Mens',
          price:  5500,
          img: require('./assets/products/p13.jpg')
        },
      ],
      cart: []
    }
   
  }, 
  methods: {
      addCart(p){
        this.cart = [...this.cart, p]
        console.log(this.cart);
      }
    }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #00292c;
  
}
*{
  margin: 0px;
  padding: 0px;
}
</style>
