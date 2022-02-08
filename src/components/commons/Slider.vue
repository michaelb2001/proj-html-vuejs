<template>
<div class="container-fluid">
 <div>
    <transition-group name="fade" tag="div">
      <div v-for="i in [currentIndex]" :key="i" class="d-flex align-items-center justify-content-center">
        <img :src="currentImg" />
      </div>
    </transition-group>
    <a class="prev" @click="prev" href="#">&#10094; Previous</a>
    <a class="next" @click="next" href="#">&#10095; Next</a>
  </div>
</div>
 
</template>
<script>
export default {
  name: "Slider",
  props: {
      images : Array
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
    }
  }
};
</script>

<style lang="scss" scoped>
@import '../../assets/style/vars.scss';
.container-fluid{
    background-color: $header-color;
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
  top: 25%;
  width: auto;
  padding: 16px;
  color: $second-text-color;
  font-weight: bold;
  font-size: 18px;
  border-radius: 0 4px 4px 0;
  text-decoration: none;
  user-select: none;
  transform: rotateZ(90deg);
  background-color: $header-text-color;
}

.next {
  right: 0;
  border-radius: 0 0 50 50;
}

.prev {
  left: 0;
  border-radius: 50 50 0 0s;
}

img{
    filter: invert(100%);
    height: 200px;
    width: 50%;
}

</style>