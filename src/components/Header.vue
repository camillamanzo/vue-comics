<template>
  <header>
      <div id="logo">
          <img id="logo-img" src="../assets/img/dc-logo.png" alt="img logo">
      </div>
      <nav id="nav-bar">
        <ul>
            <li v-for="(element, index) in links" :key="index">
                <a href="#">{{ element.name }}</a>
            </li>
        </ul>
      </nav>
  </header>
</template>

<script>
import links from './headerData';
export default {
    data(){
        return {
            links : links(),
        }
    },
}
</script>

<style lang="scss">
@import "../style/variables.scss";
@import "../style/general.scss";

    header{
        display: flex;
        justify-content: space-around;
        a{
            color: $secondaryColor;
            text-transform: uppercase;
        }
    }
    
    #logo-img{
        width: 40px;
    }


</style>