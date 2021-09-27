<template>
    <main>
        <div class="content">

        </div>
        <nav class="list-items">
            <ul>
                <li v-for="(element, index) in list" :key="index">
                <a href="#">{{ element.name }}</a>
            </li>
            </ul>
        </nav>  
    </main>
  
</template>

<script>
import list from './mainData';
export default {
    data(){
        return {
            list : list(),
        }
    },
}
</script>

<style lang="scss">
@import "../style/variables.scss";
    .content{
        height: 200px;
        background-color: $backgroundColor;
    }
</style>