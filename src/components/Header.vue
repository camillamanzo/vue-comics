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

<style lang="scss" scoped>
@import "../style/variables.scss";
    #logo-img{
        width: 10%;
    }

</style>