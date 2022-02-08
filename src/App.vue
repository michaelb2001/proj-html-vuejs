<template>
  <div id="app">
      <Header :arrayPassato="sliderImg1" />
  </div>
</template>

<script>
import Header from './components/Header.vue';


export default {
  name: 'App',
  components: {
    Header
  },
  data(){
    return{
      sliderImg1:[
        require('./assets/img/h3-rev-img-1.png'),
        require('./assets/img/h3-rev-img-3.png'),
        require('./assets/img/h3-rev-img-5.png')
      ]
    }
  }
}
</script>

<style lang="scss">
@import './assets/style/global.scss';

</style>
