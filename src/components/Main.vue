<template>
    <main>
        <div class="jumbotron">

        </div>
        <div class="current-series">
            <div class="small-container">
                <ul>
                    <li v-for="(element, index) in comics" :key="index">
                        <div class="thumbs">
                            <img :src="element.thumb" alt="">
                        </div>
                        <a href="#"><h3>{{ element.series }}</h3></a>
                    </li>
                </ul>
            </div>
            
        </div>
        <div class="list-items">
            <div class="container">
                <ul>
                    <li v-for="(element, index) in list" :key="index">
                        <h3>{{ element.name }}</h3>
                    </li>
                </ul>
            </div>
        </div>  
    </main>
  
</template>

<script>
import list from './mainData';
import comics from './mainComics';

export default {
    data(){
        return {
            list : list(),
            comics : comics(),
        }
    },
}
</script>

<style lang="scss">

@import "../style/variables.scss";
@import "../style/general.scss";

    .jumbotron{
        height: 300px;
        background-image: url(../assets/img/jumbotron.jpg);
        background-size: 100%;
    }

    .current-series{
        background-color: $secondaryColor;
          
        
        .small-container{
            width: 80%;
            margin: 0 auto;
        }
        a{
            color: $clear;
            text-transform: uppercase;
        }
        ul{
            display: flex;
            flex-wrap: wrap;
            justify-content: space-evenly;
            
            li{
                width: 150px;

                .thumbs{
                    height: 150px;
                    width: 100%;
                    overflow: hidden;
                    
                    img{
                        width: 100%;
                        height: 150%;
                        
                    }
                }
            }
        }
    }

    .list-items{
        color: $clear;
        background-color: $primaryColor;
        margin: 0 auto;

        .container{
            width: 80%;
            margin: 0 auto;
        }

        ul{
           justify-content: space-around; 
        }
        
        h3{
            font-size: 12px;
            text-transform: uppercase;
        }
    }
    
</style>