<template>
  <div class="container-fluid d-flex align-items-center justify-content-center text-start">

      <div class="row">
            <div class="col-3" v-for="(element,index) in listaPersone" :key="index">
                <img :src="element" alt="">
            </div>
      </div>

    <img src="../../assets/img/svg/svg-4.svg" class="pizzetta">
  </div>
</template>

<script>
export default {
    name:"Persone",
    data(){
        return{
            listaPersone:[
                require("../../assets/img/h1-team-1a-700x700.jpg"),
                require("../../assets/img/h1-team-2a.jpg"),
                require("../../assets/img/h1-team-3a.jpg"),
                require("../../assets/img/h1-team-4a.jpg")
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/vars.scss';
.container-fluid{
    margin: 0%!important;
    margin-top:10px!important ;
    padding: 0%!important;
    min-height: 400px;
    position: relative;
    .row{
        height: 100%;
        img{
            height: 400px;
            object-fit: contain;
        }
    }
    
    .pizzetta{
    position: absolute;
    right: 30px;
    bottom: 30px;
    background-color: $header-text-color;
    border-radius: 50%;
    padding: 5px;
    fill: $second-text-color;
}
}
</style>