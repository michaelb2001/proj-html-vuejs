<template>
<div class="container-fluid">
    <div class="container d-flex flex-row align-items-center justify-content-around text-center">
        <div class="col-3">

        </div>
        
        <div class="col-6 d-flex align-items-center">
            <img class="icon" src="../assets/img/svg/svg-0.svg" alt="">

            <ul class="d-flex align-items-center">
                <li v-for="element in menu1" :key="element.id">
                   <a href="">{{element}}</a> 
                </li>

                <img id="logo" :src="logo" alt="">

                <li v-for="element in menu2" :key="element.id">
                   <a href="">{{element}}</a> 
                </li>
            </ul>

        </div>

        <div class="col-3 d-flex align-items-center justify-content-end">
            <a href=""><img src="../assets/img/svg/svg-1.svg">Cart</a>
            <a href=""><i class="fas fa-search"></i>Search </a>
        </div>
    </div>
</div>
  
</template>

<script>
export default {
    name:"Header",
    data(){
        return{
            logo:require('../assets/img/h5-logo-divided-header.png'),
            menu1:[
                'home',
                'pages',
                'menu'
            ],

            menu2:[
                'event',
                'blog',
                'landing'
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/vars.scss';

.container-fluid{
    background-color: $header-color;
    
    .container{
        height: 100px;
        .icon{
            height: 10px;
            filter: invert(100%);
            transform: translateX(35px);
        }

        #logo{
            height: 100px;
            width: auto;
            filter: brightness(100%);
        }
        ul{
            list-style-type: none;
            margin-bottom:0%!important;
            li{
                a{
                    text-decoration: none;
                    margin: 0px 10px!important;
                    color:$header-text-color;
                    font-size :18px;
                }
            }
        }

        .col-3{
            a{
                text-decoration: none;
                color:$header-text-color;
                font-size :18px;
                margin: 0px 10px!important;
                img{
                    filter: invert(100%);
                };

                i{
                    fill: $header-text-color;
                }
            }

        }
    }
}

</style>