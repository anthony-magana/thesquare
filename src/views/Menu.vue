<template>
  <div class="Menu">
    <navbar />
    <router-view />
    <div class="menu-container">
        <h1 class="theMenu">MENU</h1>

        <div class="menu-item">
          <h3 class="menu-title">Classic Burger</h3>
          <span class="menu-price">$10</span>
          <p class="text">Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
            sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
          </p>
        </div>

        <div class="menu-item">
          <h3 class="menu-title">Double Cheese Burger</h3>
          <span class="menu-price">$14</span>
          <p class="text">Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
            sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
          </p>
        </div>

        <div class="menu-item">
          <h3 class="menu-title"> Pepperoni Pizza</h3>
          <span class="menu-price">$10</span>
          <p class="text">Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
            sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
          </p>
        </div>

        <div class="menu-item">
          <h3 class="menu-title">3 Steak Tacos</h3>
          <span class="menu-price">$12</span>
          <p class="text">Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
            sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
          </p>
        </div>
        <hr>
        <h1 class="theMenu">SIDES</h1>
        <div class="sides-item">
          <span class="sides">Fries</span>
          <span class="price">$4</span>
        </div>

        <div class="sides-item">
          <span class="sides">5 Pc Chicken Strips</span>
          <span class="price">$6</span>
        </div>

        <div class="sides-item">
          <span class="sides">Chilli Cheese Fries</span>
          <span class="price">$6</span>
        </div>
        <hr>
        <h1 class="theMenu">DRINKS</h1>
        <div class="sides-item">
          <span class="sides">Soda</span>
          <span class="price">$2</span>
        </div>

        <div class="sides-item">
          <span class="sides">Milk Shake</span>
          <span class="price">$3.50</span>
        </div>

        <hr>
        <h1 class="theMenu">DESSERTS</h1>
        <div class="menu-item">
          <h3 class="menu-title">Ice-Cream Roll</h3>
          <span class="menu-price">$6</span>
          <p class="text">Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
            sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
          </p>
        </div>

        <div class="menu-item">
          <h3 class="menu-title">Cheese Cake</h3>
          <span class="menu-price">$6</span>
          <p class="text">Lorem ipsum dolor sit amet, consectetur adipiscing elit, 
            sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.
          </p>
        </div>
    </div>
    <footerComp />
  </div>
</template>

<script>
// @ is an alias to /src
import navbar from '@/components/navbar.vue'
import footerComp from '@/components/footerComp.vue'


export default {
  name: 'foodmenu',
  components: {
    navbar,
    footerComp
  }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css?family=Lato|Courgette|Open+Sans&display=swap');

    .menu-container{
        margin-top: 100.5px;
        margin-left: 20vw;
        margin-right: 20vw;
    }
    .menu{
        margin: 0;
    }
    .theMenu{
      top: 0;
      bottom: 0;
      padding: 30px 0;
      padding-left: 40px;
      font-family: 'Lato', sans-serif;
      font-size: 36px;
      color: rgb(199, 0, 0);
        
    }
    .menu-item{
      padding-bottom: 30px;
      padding-left: 40px;
      padding-right: 30px;
      font-family: 'Open Sans', sans-serif;
    }
    .menu-title{
      font-family: Helvetica, sans-serif;
    }
    .text{
      color: #555;
    }
    .menu-price{
      float: right;
      font-size: 26px;
      padding: 0px 0 0 20px;
    }
    .sides-item{
      padding-top: 10px;
      padding-bottom: 30px;
      padding-left: 40px;
      padding-right: 30px;
      font-family: 'Open Sans', sans-serif;
      font-size: 26px;
      line-height: 1.25em;
    }
    .sides{
      font-family: Helvetica, sans-serif;
    }
    .price{
      float: right;
    }

    @media (max-width: 850px){
      .menu-container{
        margin-left: 0;
        margin-right: 0;
      }
      .theMenu{
        font-size: 30px;
      }
      .menu-title{
        font-size: 24px;
      }
      .text{
        font-size: 14px;
      }
      .menu-price{
        font-size: 24px;
      }
      .sides-item{
        font-size: 24px;
      }
    }
</style>