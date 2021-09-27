<template>
    <main>
        <div class="jumbotron">

        </div>
        <div class="current-series">
            <ul>
                <li v-for="(element, index) in comics" :key="index">
                    <img :src="element.thumb" alt="">
                    <a href="#"><h3>{{ element.series }}</h3></a>
                    
                </li>
            </ul>
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

    .container{
        width: 80%;
        margin: 0 auto;
    }
    .jumbotron{
        height: 300px;
        background-image: url(../assets/img/jumbotron.jpg);
        background-size: 100%;
    }

    .current-series{
        background-color: $secondaryColor;
        a{
            color: $clear;
        }
    }

    .list-items{
        color: $clear;
        background-color: $primaryColor;
        
        h3{
            font-size: 12px;
        }
    }
    
</style>