<template>
<div>
<div class="holder">
    <div v-bind:key="product.id" v-for="product in products" class="product">
    <img v-bind:src="product.img" v-bind:alt='product.price'>
            <p>{{product.name}}</p>
        <div> 
            <h4>{{product.price}}</h4>
            <button class="btn" v-on:click="$emit('add-cart', product)"> Add to cart</button>
        </div>
       
    </div>
    </div>
</div>
</template>

<script>

export default {
    name: "Products",
    props: ["products"],
    // methods: {
    //     addToCart(p){
    //         console.log(p);
    //     }
    // }
}
</script>

<style scoped>
.holder{
    width: 100%;
    max-width: 780px;
    margin: 50px auto;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-around;
}
    .product{
        width: 200px;
        height: 300px;
        
    }
    .product>div{
        display: flex;
        justify-content: space-evenly;
        align-items: center;

    }
    .btn{
        padding: 10px;
        border: none;
        border-radius: 2px;
        background: #9DC79F;
    }
    img{
        width: 100%;
        }

</style>