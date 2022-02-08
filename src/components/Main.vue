<template>
  <div class="container-fluid">
      <Carte :immaginiCarte="arrayImgCartePassato" />
      <Slider2 :caption="arrayPerSecondoSlider"/>
      <Pizzaspecial />
  </div>
</template>

<script>
import Carte from './commons/Carte.vue';
import Slider2 from './commons/Slider2.vue';
import Pizzaspecial from './commons/Pizzaspecial.vue';
export default {
    name: "Main",
    components:{
      Carte,
      Slider2,
      Pizzaspecial

    },
    props:{
      arrayImgCartePassato : Array,
      arrayPerSecondoSlider : Array
    }
}
</script>

<style lang="scss" scoped>
.container-fluid{
    padding: 0%!important;
    margin: 0%!important;
}
</style>