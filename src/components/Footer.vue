<template>
  <footer>
        <div class="top-footer">
            <nav class="left">
                <div>
                    <h3>DC Comics</h3>
                    <ul>
                        <li v-for="(element, index) in comics" :key="index">
                            <a href="#">{{ element.name }}</a>
                        </li>
                    </ul>
                    <h3>Shop</h3>
                    <ul>
                        <li v-for="(element, index) in shop" :key="index">
                            <a href="#">{{ element.name }}</a>
                        </li>
                    </ul>
                </div>
                <div>
                    <h3>DC</h3>
                    <ul>
                        <li v-for="(element, index) in DC" :key="index">
                            <a href="#">{{ element.name }}</a>
                        </li>
                    </ul>
                </div>
                
                <div>
                    <h3>Sites</h3>
                    <ul>
                        <li v-for="(element, index) in sites" :key="index">
                            <a href="#">{{ element.name }}</a>
                        </li>
                    </ul>
                </div>
                
            </nav>
            <div class="right">
                <img id="footer-logo" src="../assets/img/dc-logo-bg.png" alt="">
            </div>
        </div>
        <div class="bottom-footer">
            <button>Sign-up now</button>
            <div>
                <h4>Follow us now</h4>
                <img class="footer-logo-img" src="../assets/img/footer-facebook.png" alt="facebook logo">
                <img class="footer-logo-img" src="../assets/img/footer-facebook.png" alt="twitter logo">
                <img class="footer-logo-img" src="../assets/img/footer-facebook.png" alt="youtube logo">
                <img class="footer-logo-img" src="../assets/img/footer-facebook.png" alt="pinterest logo">
                <img class="footer-logo-img" src="../assets/img/footer-facebook.png" alt="pinterest logo">
            </div>
      </div>
  </footer>
</template>

<script>
import footerComics from './footerComics';
import footerShop from './footerShop';
import footerDC from './footerDC';
import footerSites from './footerSites';

export default {
    data(){
        return {
            comics : footerComics(),
            shop : footerShop(),
            DC : footerDC(),
            sites : footerSites(),
        }
    },
}
</script>

<style lang="scss">
@import "../style/variables.scss";
@import "../style/general.scss";
    .top-footer{
        background-image: url(../assets/img/footer-bg.jpg);
        display: flex;
        height: 400px;
        overflow: hidden;
        align-items: center;

        img{
            width: 120%;
        }
        a{
            color: $clear;
        }
        .left{
            height: 100%;
            width: 50%;
            padding: 50px 0 50px 100px;
            display: flex;
            
            ul{
                display: flex;
                flex-direction: column;
            }
        }
        
    }

    h3{
        color: $clear;
    }

    .bottom-footer{
        background-color: $lighterBackgroundColor;
        
    }
    .footer-logo-img{
            width: 30px;
    }

</style>