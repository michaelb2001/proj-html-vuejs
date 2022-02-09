<template>
  <div class="container-fluid d-flex align-items-center justify-content-center">
      <div class="col-10 d-flex align-items-center justify-content-center">
          <div class="col-2"
            v-for="(element,index) in listaSponsor" :key="index">
            <img :src="element" alt="">
          </div>
      </div>
  </div>
</template>

<script>
export default {
    name:"Sponsor",
    data(){
        return{
            listaSponsor:[
                require("../../assets/img/h1-clients-img-1.png"),
                require("../../assets/img/h1-clients-img-2.png"),
                require("../../assets/img/h1-clients-img-3.png"),
                require("../../assets/img/h1-clients-img-4.png"),
                require("../../assets/img/h1-clients-img-5.png"),
            ]
        }
    }
}
</script>

<style lang="scss" scoped>

@import '../../assets/style/vars.scss';

.container-fluid{
    background-color: $background-color-fisrt;
    .col-10{
        padding:20px 0px!important;
    }
    img{
        width: 100%;
    };
}
</style>