<template>
  <div class="container-fluid">
      <div class="row">
          <div class="col-6 d-flex align-items-center justify-content-center text-center sfondo">
              <img src="../../assets/img/h1-img-7n.png" alt="">
          </div>
          <div class="col-6 d-flex align-items-center justify-content-center text-start testo">
              <div class="col-8">
                <h1>SPECIAL *</h1>

                <p>lorem ipsum dolor sit amet , consectur adisìping
                    elit. Praesent ut.
                </p>

                <div class="special">
                    <div class="d-flex align-items-center justify-content-start text-start">
                        <h2 class="prezzo">$10 </h2> 
                        <h2 class="ms-3">COMBO PICCOLO</h2>
                    </div>
                    <p>Lorem ispum dolor sit amet, consectetur adisìping elit.
                        Praesent ut aliquam dui.
                    </p>
                </div>
                
                
                <div class="special ">
                    <div class="d-flex align-items-center justify-content-start text-start">
                        <h2 class="prezzo">$10 </h2> 
                        <h2 class="ms-3">COMBO MEDIO</h2>
                    </div>

                    <p>Lorem ispum dolor sit amet, consectetur adisìping elit.
                        Praesent ut aliquam dui.
                    </p>
                </div>


                
                <div class="special">
                    <div class="d-flex align-items-center justify-content-start text-start">
                        <h2 class="prezzo">$10 </h2> 
                        <h2 class="ms-3">COMBO GRANDE</h2>
                    </div>
                    <p>Lorem ispum dolor sit amet, consectetur adisìping elit.
                        Praesent ut aliquam dui.
                    </p>
                </div>
              </div>

          </div>
      </div>
  </div>
</template>

<script>
export default {
    name:"Pizzaspecial"
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/vars.scss';

.container-fluid{
    padding: 0%!important;
    margin: 0%!important;
}

.col-6{
    min-height: 500px;
}

.col-6.sfondo{
    background-image: url("../../assets/img/h1-img-4.jpg");
    background-size: cover;
    background-repeat: no-repeat;
}

.col-6.testo{
    background-color: $header-text-color;

}

.testo{
    div{
        
        h2.prezzo{
            color: $third-text-color;
        }
    }
}
</style>