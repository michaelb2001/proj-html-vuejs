<template>
  <div class="container-fluid">
      <Carte :immaginiCarte="arrayImgCartePassato" />
  </div>
</template>

<script>
import Carte from './commons/Carte.vue'
export default {
    name: "Main",
    components:{
      Carte
    },
    props:{
      arrayImgCartePassato : Array
    }
}
</script>

<style lang="scss" scoped>
.container-fluid{
    padding: 0%!important;
    margin: 0%!important;
}
</style>