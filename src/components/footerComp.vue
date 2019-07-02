<template>
  <div class="footer-con">
    <hr>
    <div class="social">
      <a href="https://www.facebook.com" target="_blank"><i class="fa fa-facebook-official" aria-hidden="true"></i></a>
      <a href="https://www.instagram.com" target="_blank"><i class="fa fa-instagram" aria-hidden="true"></i></a>
      <a href="https://www.twitter.com" target="_blank"><i class="fa fa-twitter" aria-hidden="true"></i></a>
    </div>

    <hr>

    <p class="pcon">
      Copyright &copy; 2019 TheSquare - All Rights Reserved.
    </p>
  </div>
</template>

<script>
export default {
  name: 'footerComp',

  data: {
    aLink: true
  },
  methods: {
    link: function(){

    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

p{
  text-align: center;
  font-size: 16px;
  font-family: 'Open Sans', sans-serif;
}
.footer-con{
  display: inline;
  margin: 0;
}
.pcon{
  margin: 0;
  padding: 30px 0;
}
.social{
  display: block;
  /* color: black; */
  float: center;
  text-align: center;
  line-height: 80px;
  font-size: 48px;
  cursor: pointer;
  padding: 0 20px;
}
.social i{
  padding: 0 4vw;
}
.social a{
  color: rgb(199, 0, 0);
}
.social a:hover{
  opacity: 0.8;
}

@media (max-width: 850px){
  .pcon{
    padding: 30px 20px;
  }
  .social{
    font-size: 40px;
  }
  
}
</style>