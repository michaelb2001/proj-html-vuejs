<template>
  <div class="container-fluid d-flex flex-column align-items-center justify-content-center text-center mt-5">
    <div class="row align-items-center justify-content-center text-center mt-5 prima_row">
        <div class="col-5">
            <h5>choose your flavor</h5>
            <h2>THE BEST PIZZA MENU IN TOWN</h2>
            <h4>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Veniam molestias eligendi illo.</h4>
        </div>

        <img src="../../assets/img/svg/svg-4.svg" class="pizzetta">
    </div>

    <div class="row mt-2">
        <div class="col-2 align-items-center justify-content-center text-center"
        v-for="(element,index) in listaPizze" :key="index">
            <img :src="element.img" :alt="element.nome" >
            <p class="nome_pizza">{{element.nome}}</p>
        </div>
    </div>

    <img src="../../assets/img/svg/svg-10.svg" class="cerchiolino">
  </div>
</template>

<script>
export default {
    name:"Pizze",
    data(){
        return{
            listaPizze:[
                {
                    nome: "bismark",
                    img:require("../../assets/img/h3-product-img-1a-100x100.png")
                },
                {
                    nome: "fiori di zucca",
                    img:require("../../assets/img/h3-product-img-2a-150x150.png")
                },
                {
                    nome: "valdostana",
                    img:require("../../assets/img/h3-product-img-3a-150x150.png")
                },
                {
                    nome: "pizza tartufata",
                    img:require("../../assets/img/h3-product-img-4a-150x150.png")
                },
                {
                    nome: "francescana",
                    img:require("../../assets/img/h3-product-img-5a-150x150.png")
                },
                {
                    nome: "campagnola",
                    img:require("../../assets/img/h3-product-img-6a-100x100.png")
                }
                
                
            
                
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/vars.scss';

img{
    width: 150px;
    height: 150px;
}

h5,.nome_pizza{
 color: $third-text-color;
}
.prima_row{
    position: relative;
    width: 100%;
}
.pizzetta{
    position: absolute;
    right: 30px;
    bottom: 30px;
    background-color: $header-text-color;
    border-radius: 50%;
    padding: 5px;
    fill: $second-text-color;
    width: 28px;
    height: 33px;
}

.cerchiolino{
    position: absolute;
    right: 10px;
    bottom: 0px;
    background-color: $third-text-color;
    padding: 5px;
    fill: $second-text-color;
    width: 28px;
    height: 33px;
}
</style>