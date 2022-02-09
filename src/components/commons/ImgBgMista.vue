<template>
  <div class="container-fluid d-flex align-items-center justify-content-center text-start">
      <h2>
          GO AHEAD AND BUILD YOUR OWN PIZZA <br>
          WE DON'T JUDGE
      </h2>

    <img src="../../assets/img/svg/svg-4.svg" class="pizzetta">
  </div>
</template>

<script>
export default {
    name:"ImgBgMista"
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/vars.scss';
.container-fluid{
    margin: 0%!important;
    padding: 0%!important;
    height: 600px;

    background-image: url("../../assets/img/h3-background-img.jpg");
    background-size: cover;
    background-repeat: no-repeat;

    position: relative;

    h2{
        position: absolute;
        top: 50%;
        left: 30%;
        transform: translate(-50%,-30%);
        width: 200px;
        color: $header-text-color;
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
}
</style>