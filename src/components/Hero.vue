<template>
    <div class="hero">
        <Nav v-bind:cart="cart"/>
        <header>
            <div class="holder">
                 <div class="textHolder">
                <h1>Styles</h1>
                <h2>For <em style='color: white'>You</em></h2>
                <button>Shop now</button>
            </div >
            <div class="imageHolder">
                    <div class="circle"></div>
                    <img src="../assets/plain.png" alt="" >
            </div>
            </div>
           

        </header>
    </div>
</template>
<script>
import Nav from "./Nav";
export default {
    name: 'Hero',
    components: {
        Nav
    },
    props: ['cart']
}
</script>

<style scoped>

    header{
        height: 500px;
        background: url('../assets/herobg.png');
        background-size: cover;
        background: #9DC79F;
        
    }
    .holder{
        display: flex;
        width: 100%;
        max-width: 780px;
        margin:  auto;
        padding: 100px 0px;
    }
    .textHolder{
        flex: 1;
    }
    .textHolder>h1{
        font-size: 5em;
        font-weight: normal;
    }
    .textHolder>h2{
        font-size: 3em;
        font-weight: normal;
        margin-bottom: 20px;
    }

    .imageHolder{
        flex: 1;
        position: relative;
    }
    .imageHolder>.circle{
        width: 300px;
        height: 300px;
        border-radius: 100%;
        background: aliceblue;
        position: absolute;
        top: 0px;
        left: 10%;
        z-index: 1;
        box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
        transition: .5s ease-in-out;
    }
    .imageHolder>.circle:hover{
        background: rgb(219, 231, 226);

    }
    .imageHolder>img{
        width: 200px;
        position: absolute;
        top: -20px;
        left: 22%;
        z-index: 2;
    }
    button{
        padding: 10px;
        border: none;
        border-radius: 5px;
        background: white;
    }
</style>