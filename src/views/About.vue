<template>
  <div class="about">
    <navbar />
    <!-- BOOTSTRAP+VUE GRID -->
    <b-container class="bv-example-row">
      <b-row>
        <b-col sm="6" xs="2" cols="6" >
          <h1 class="page-heading">Our Story</h1>
          <p class="text">Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.
             It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. 
             It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
          </p>
        </b-col>

        <b-col sm="6" cols="6">
          <div class="our-story"><img src="@/assets/about-page/our-story.jpg" alt="Our Story"></div>
        </b-col>
      </b-row>

      <b-row>
        <b-col sm="6" cols="6">
          <div class="our-staff"><img src="@/assets/about-page/our-staff.jpg" alt="Our Story"></div>
        </b-col>

        <b-col sm="6" cols="6">
            <h1 class="page-heading ourstaff">Our Staff</h1>
            <p class="text ourstaff">Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.
              It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged. 
              It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
            </p>
          </b-col>
      </b-row>

      <b-row>
        <b-col sm="6" cols="6">
          <h1 class="page-heading">Visit Us</h1>
          <p class="text">Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.
             It has survived not only five centuries, but also the leap into electronic typesetting, remaining essentially unchanged.
             It was popularised in the 1960s with the release of Letraset sheets containing Lorem Ipsum passages, and more recently with desktop publishing software like Aldus PageMaker including versions of Lorem Ipsum.
          </p>
          <div class="where">
            <button class="visit"><router-link to="/contact"><p class="visit-txt">Visit</p></router-link></button>
          </div>
        </b-col>

        <b-col sm="6" cols="6">
          <div class="visit-us"><img src="@/assets/about-page/visit-us.jpg" alt="Our Story"></div>
        </b-col>
      </b-row>

    </b-container> 
    <footerComp />
  </div>
</template>

<script>
// @ is an alias to /src
import navbar from '@/components/navbar.vue'
import footerComp from '@/components/footerComp.vue'

export default {
  name: 'about',
  components: {
    navbar,
    footerComp
  },

}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css?family=Lato|Courgette|Open+Sans&display=swap');

.about{
  margin-top: 100.5px;
}
.page-heading{
  top: 0;
  bottom: 0;
  padding: 40px 0 10px 0;
  font-family: 'Courgette', sans-serif;
  font-size: 36px;
  /* color: rgb(199, 0, 0); */
}
img {
  border: 1px solid #ddd;
  padding: 5px;
  max-width: 420px;
  max-height: 480px;
}
.our-story{
  padding: 40px 0px 0px 30px;
}
.our-staff{
  padding: 40px 30px 0px 0px;
}
.visit-us{
  padding: 40px 0px 20px 30px;
}
.text{
  padding: 0 30px 0 0;
  color: rgb(94, 94, 94);
  margin: 0;
  font-family: 'Open Sans', sans-serif;
}

.where{
  float: left;
  padding: 25px 30px 30px 0;
}
.visit{
  border: none;
  background-color: transparent;
  color: #dc3545;
  border: 1px solid #dc3545;
  border-radius: 12px;
  text-align: center;
}
.visit:hover{
  background-color: #dc3545;
}
.visit-txt{
  margin: 0;
  padding: 8px 30px;
  color: #dc3545;
}
button{
  padding: 0;
}
a{
  text-decoration: none;
}
.visit-txt:hover{
  color: white;
}
@media (max-width: 993px){
  img{
    max-width: 35vw;
    max-height: 480px;
  }
  .text{
    font-size: 14px;
  }
  .page-heading{
    font-size: 32px;
  }
  .ourstaff{
    padding-left: 4vw;
  }
  
}

@media (max-width: 500px) {
  .col-6{
    max-width: 100%;
    flex: none;
    display: inline;
  }
  .text{
    padding: 30px;
    padding-top: 20px;
    display: inline;
  }
  .page-heading{
    margin: 0;
    padding-top: 20px;
    padding-left: 10px;
  }
  .our-story{
    padding: 0;
    float: right;
  }
  .our-staff{
    padding: 0;
    float: left;
  }
  .visit-us{
    padding: 0;
    float: right;
  }
}

</style>
