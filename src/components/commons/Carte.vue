<template>
  <div class="container-fluid">
      <div class="row py-2 px-0">
          <div class="col-3 align-items-center justify-content-center"
          v-for="(element,index) in immaginiCarte" :key="index">
              <img :src="element">
          </div>
      </div>
  </div>
</template>

<script>
export default {
    name:"Carte",
    props:{
        immaginiCarte : Array
    }
}
</script>

<style lang="scss" scoped>
.container-fluid{
    padding: 0%!important;
    margin: 0%!important;
}
img{
    width:100%
}
</style>