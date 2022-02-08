<template>
  <div id="app">
      <Header :arrayPassato="sliderImg1" 
              :arrayPizzaPassato="sliderImg1Pizza" />
      <Main />
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
      ]
    }
  }
}
</script>

<style lang="scss">
@import './assets/style/global.scss';

</style>
