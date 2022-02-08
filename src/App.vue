<template>
  <div id="app">
      <Header :arrayPassato="sliderImg1" 
              :arrayPizzaPassato="sliderImg1Pizza" />
      <Main :arrayImgCartePassato="imgCarte"/>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Main from './components/Main.vue';


export default {
  name: 'App',
  components: {
    Header,
    Main
  },
  data(){
    return{
      sliderImg1:[
        require('./assets/img/h3-rev-img-1.png'),
        require('./assets/img/h3-rev-img-3.png'),
        require('./assets/img/h3-rev-img-5.png')
      ],

      sliderImg1Pizza:[
          require('./assets/img/h3-rev-img-2.png'),
          require('./assets/img/h3-rev-img-4.png'),
          require('./assets/img/h3-rev-img-6.png')
      ],

      imgCarte:[
        require('./assets/img/h3-img-1.jpg'),
        require('./assets/img/h3-img-2.jpg'),
        require('./assets/img/h3-img-3.jpg'),
        require('./assets/img/h3-img-4.jpg'),

      ]
    }
  }
}
</script>

<style lang="scss">
@import './assets/style/global.scss';
#app{
  overflow: hidden;
}
</style>
