<template>
<div class="container-fluid">
 <div>
    <transition-group name="fade" tag="div">
      <div v-for="i in imagesPizza" :key="i" class="d-flex align-items-center justify-content-center">
        <img class="z_index" :src="currentImgPizza" />
      </div>

      <div v-for="(i,index) in images" :key="index" class="d-flex align-items-center justify-content-center">
        <img class="sfondo" :src="currentImg" />
      </div>
    </transition-group>
    <a class="prev" @click="prev" href="#">Pre</a>
    <a class="next" @click="next" href="#"> Next</a>
  </div>
</div>
 
</template>

<script>
export default {
  name: "Slider",
  props: {
      images : Array,
      imagesPizza : Array
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
    },
    prev: function() {
      this.currentIndex -= 1;
    }
  },

  computed: {
    currentImg: function() {
      return this.images[Math.abs(this.currentIndex) % this.images.length];
    },
    currentImgPizza: function(){
      return this.imagesPizza[Math.abs(this.currentIndex) % this.imagesPizza.length];
    }
  }
};
</script>

<style lang="scss" scoped>
@import '../../assets/style/vars.scss';
.container-fluid{
    background-color: $header-color;
    min-height: 350px;
}

.fade-enter,
.fade-leave-to {
  visibility: hidden;
  width:100%;
  opacity: 0;
}

img {
  height:600px;
  width:100%
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
}

.next {
  right: 0%!important;
  border-radius: 0 0 50% 50%!important;
}

.prev {
  left: 0%!important;
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
    top: 50%;
    left: 50%;
    transform: translate(-50%,-50%);
}
</style>