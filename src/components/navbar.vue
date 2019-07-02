<template>
  <div class="nav-container">
    <div class="logo"><img src="@/assets/logo.png" alt="TheSquare"></div>
      <nav class="active " v-bind:class="{'toggleActive': isActive}">
        <ul>
          <li><router-link to="/">HOME</router-link></li>
          <li><router-link to="/foodmenu">MENU</router-link></li>
          <li><router-link to="/contact">CONTACT</router-link></li>
          <li><router-link to="/about">ABOUT</router-link></li>
        </ul>
      </nav>
    <div class="menu-toggle" @click="toggleClass">
      <i class="fa fa-bars" aria-hidden="true"></i>
    </div>
    <router-view/>
  </div>
</template>

<script>
export default {
  name: 'navbar',
  props: {
    msg: String
  },
  data: function() {
    return{
      isActive: false
    }
  },
  methods: {
    toggleClass: function(){
      this.isActive = !this.isActive;
      
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.nav-container{
  top: 0;
  left: 0;
  position: absolute;
  padding: 0 100px;
  width: 100%;
  box-sizing: border-box;
  background: #fcfcfc;
  border-bottom: 1px solid rgba(0, 0, 0, 0.1);
}

.logo{
  text-align: center;
  float: left;
  padding-top: 12px;
  padding-bottom: 12px;
  padding-left: 3%;
  padding-right: 5vw;
}

img{
  width: 60px;
  height: 60px;
  line-height: 60px;
  float: left;
}

nav{
  float: right;
}
nav ul{
  margin: 0;
  padding: 0;
  display: flex;
}
nav ul li{
  list-style: none;
  padding: 25px 0;
  padding-right: 20px;

}
nav ul li a{
  height: 50px;
  line-height: 50px;
  padding: 0 20px;
  color: #333;
  text-decoration: none;
  font-size: 16px;
}
nav ul li a:hover,
nav ul li a.router-link-exact-active{
  color: red;
}

.menu-toggle{
  color: black;
  float: right;
  line-height: 65px;
  font-size: 26px;
  cursor: pointer;
  display: none;
}

@media (max-width: 850px){
  .nav-container{
    padding: 0 6%;
    position: fixed;
    z-index: 16;
  }
  .menu-toggle{
    display: block;
    padding-top: 10px;
  }
  .logo{
    padding-left: 3%;
  }
  nav{
    /* display: none; */
    position: absolute;
    width: 100%;
    height: 100vh;
    background: #000;
    opacity: 0.87;
    top: 85px;
    left: -100%;
    transition: 0.5s;
  }
  .router-link-exact-active{
    left: 1;
  }
  .toggleActive{
    left: 0;
    z-index: 16;
  }
  nav ul{
    display: block;
    text-align: center;
    padding-top: 50px;
  }
  nav ul li a{
    color: #f7f7f7;
    font-size: 20px;
  }
}
</style>
