<template>
<div class="container-fluid d-flex justify-content-center align-items-center text-center p-5">
 <div>
    <transition-group name="wave" tag="div">
      <div v-for="(element,index) in caption" :key="index" class="item hidden text-center p-5" 
        :class="{active : isActive(index) }">
      <div>
            <h3>{{element.motto}}</h3>
            <p>{{element.sub_motto}}</p>
        </div>
      </div>
    </transition-group>
    <a class="prev" @click.prevent="prev" href="#">Pre</a>
    <a class="next" @click.prevent="next" href="#"> Next</a>
  </div>

  <img src="../../assets/img/svg/svg-4.svg" class="pizzetta">
</div>
 
</template>

<script>
export default {
  name: "Slider2",
  props: {
      caption: Array
  },
data() {
    return {
      timer: null,
      currentIndex: 0
    };
  },

  mounted: function() {
    this.startSlide();
  },

  methods: {
    startSlide: function() {
      this.timer = setInterval(this.next, 4000);
    },

    next: function() {
      this.currentIndex += 1;
      console.log(this.currentIndex);
      if(this.currentIndex == this.caption.length){
        this.currentIndex = 0;
      }
      
    },
    prev: function() {
      this.currentIndex -= 1;
       console.log(this.currentIndex);
      if(this.currentIndex == 0){
        this.currentIndex = this.caption.length-1;
      }
    },
    isActive:function(indice){
      return indice == this.currentIndex;
    }
  }
};
</script>

<style lang="scss" scoped>
@import '../../assets/style/vars.scss';
.container-fluid{
    background-color: $header-color;
    min-height: 350px;
    background-image: url("../../assets/img/h3-testimonials-bckgrnd.jpg");
    background-size: cover;
    background-repeat: no-repeat;
    position: relative;
}

.wave-enter,
.wave-leave-to {
  visibility: hidden;
  width:100%;
  opacity: 0;
}

.motto{
  width:100%;
  display: none;
}

.prev, .next {
  cursor: pointer;
  position: absolute;
  top: 45%;
  width: auto;
  padding: 16px;
  color: $second-text-color;
  font-weight: bold;
  font-size: 18px;
  text-decoration: none;
  user-select: none;
  transform: rotateZ(90deg);
  background-color: $header-text-color;
  width: 80px;
  text-align: center;
}

.next {
  right: -10px!important;
  border-radius: 0 0 50% 50%!important;
}

.prev {
  left: -1%!important;
  border-radius: 50% 50% 0 0!important;
}

.sfondo{
    filter: invert(100%);
    height: 200px;
    width: 50%;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
}

.z_index{
    z-index:999;
    height: 250px;
    width:auto;
    position: absolute;
    top: 35%;
    left: 50%;
    transform: translate(-50%,-35%);
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
.hidden{
  display: none!important;
}
.active{
  display: flex!important;
  align-items:center!important;
  justify-content: center!important;
}
</style>