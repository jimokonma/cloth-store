<template>
    <div class="navbar">
        <nav>
        <img src="../assets/logo.png" alt="" class="logo">
            <ul>
                <li> Home </li>
                <li>Catigories </li>
                <li v-on:click="()=>viewCheck=!viewCheck">Cart 
                    <span class="cartNotify">
                    {{cart.length}}
                    
                    </span>
                     <span class="cart" v-bind:class="{'display':viewCheck}">
                        <span class="cart-item" v-bind:key="item.id" v-for="item in cart.slice(0,3)">

                        <img v-bind:src="item.img" v-bind:alt="item.name">
                        <p>{{item.name}}</p>
                        <button>x</button>
                        </span>

                        <button >Check out</button>
                    </span>
                    </li>  
            </ul>
        </nav>
    </div>
</template>
<script>
export default {
    name: 'Nav',
    props: ['cart'],
    data(){
        return{
            viewCheck: false
        }
    }
}
</script>

<style scoped>
.navbar{
    box-shadow: 5px 5px 5px 5px;
    background: #9DC79F;
    /* position: absolute; */

}
nav{
    width: 90%;
    height: 60px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: 0px auto;
    z-index: 1;
}
ul{
    width: 300px;
    list-style: none;
    display: flex;
    justify-content: space-evenly;
}
.cartNotify{
    font-size: .8em;
    padding: 3px 5px;
    background: rgb(223, 6, 6);
    color: white;
    border-radius: 50%;
    position: absolute;
    right: -15px;
    top: -10px;
}
li:last-child{
    position: relative;
    cursor: pointer;
}
.logo{
    width: 35px;
}
.cart{
    position: absolute;
    width: 100px;
    min-height: 100px;
    padding: 5px;
    top: 20px;
    right: -50px;
    background: white;
    display: none;

    
    
}
.display{
    display: block;
}
.cart-item{
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: .5em;
    border-bottom: 1px solid rgb(228, 228, 228);
}
.cart-item>img{
    width: 30px;
    border-radius: 50%;
    display: flex;
    z-index: 1;
}
button{
    border: none;
    padding: 2px;
    color: #9DC79F;
    background: none;
    cursor: pointer;
}
</style>