<template>
  <div class="container-body">
    <!-- NAVIGATION -->
    <navbar />
    <router-view />
        <h1>Welcome to The Square</h1>
        <div class="button">
            <b-button @click="linkcontact()" variant="outline-danger">Call Now</b-button>
        </div>
        <hr>
        <!-- CAROUSEL PHOTOGALLERY -->
        <h2>PHOTO GALLERY</h2>
        <div class="carousel-con">
            <b-carousel
                id="carousel-1"
                v-model="slide"
                :interval="4000"
                controls
                indicators
                background="#ababab"
                img-width="1024"
                img-height="480"
                style="text-shadow: 1px 1px 2px #333;"
                @sliding-start="onSlideStart"
                @sliding-end="onSlideEnd"
            >
                <!-- Text slides with image -->
                <b-carousel-slide
                    caption="First slide"
                    text="Nulla vitae elit libero, a pharetra augue mollis interdum.">
                    <img slot="img" src="@/assets/slide-images/cooking.jpg"
                    class="d-block img-fluid w-100"
                    width="1024"
                    height="480">
                </b-carousel-slide>

                <!-- Slides with custom text -->
                <b-carousel-slide caption="Second slide"
                    text="Nulla vitae elit libero, a pharetra augue mollis interdum.">
                    <img slot="img" src="@/assets/slide-images/pizza-pepperoni.jpg"
                    class="d-block img-fluid w-100"
                    width="1024"
                    height="480">
                </b-carousel-slide>
                
                <b-carousel-slide caption="Third slide"
                    text="Nulla vitae elit libero, a pharetra augue mollis interdum.">
                    <img slot="img" src="@/assets/slide-images/tacos-steak.jpg"
                    class="d-block img-fluid w-100"
                    width="1024"
                    height="480">
                </b-carousel-slide>

                <b-carousel-slide caption="Third slide"
                    text="Nulla vitae elit libero, a pharetra augue mollis interdum.">
                    <img slot="img" src="@/assets/slide-images/icecream-rolls.jpg"
                    class="d-block img-fluid w-100"
                    width="1024"
                    height="480">
                </b-carousel-slide>

                <b-carousel-slide caption="Fourth slide"
                    text="Nulla vitae elit libero, a pharetra augue mollis interdum.">
                    <img slot="img" src="@/assets/slide-images/dessert.jpg"
                    class="d-block img-fluid w-100"
                    width="1024"
                    height="480">
                </b-carousel-slide>

                <!-- Slide with blank fluid image to maintain slide aspect ratio -->
                <b-carousel-slide caption="Blank Image" img-blank img-alt="Blank image">
                    <p class="blank-img">
                    Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse eros felis, tincidunt
                    a tincidunt eget, convallis vel est. Ut pellentesque ut lacus vel interdum.
                    </p>
                    <button @click="linkmenu()" class="btn-caro">Learn More</button>
                </b-carousel-slide>
            </b-carousel>
        </div>
        <!-- LOCATION -->
        <h4 class="brand">The Square</h4>
        <p class="location">1351  Sunny Day Drive, Los Angeles, California </p>
        <p class="location">90017, United States</p>
        <p class="phone">(714)-810-4275</p>

        <!-- TABLE FOR HOURS OPEN -->
        <h4>Hours</h4>
        <div class="table-con">
            <table align="center">
                <tr>
                    <th></th>
                    <th></th>
                </tr>
                <tr>
                    <td>Mon</td>
                    <td>11:00 am - 12:00 am</td>
                </tr>
                <tr>
                    <td>Tue</td>
                    <td>11:00 am - 12:00 am</td>
                </tr>
                <tr>
                    <td>Wed</td>
                    <td>11:00 am - 12:00 am</td>
                </tr>
                <tr>
                    <td>Thur</td>
                    <td>11:00 am - 12:00 am</td>
                </tr>
                <tr>
                    <td>Fri</td>
                    <td>11:00 am - 12:00 am</td>
                </tr>
                <tr>
                    <td>Sat</td>
                    <td>11:00 am - 12:00 am</td>
                </tr>
                <tr>
                    <td>Sun</td>
                    <td>11:00 am - 12:00 am</td>
                </tr>
            </table>
        </div>
        <footerComp />
    </div>
</template>

<script>
// @ is an alias to /src
import navbar from '@/components/navbar.vue'
import footerComp from '@/components/footerComp.vue'

export default {
  name: 'home',
  components: {
    navbar,
    footerComp
  },
    data: function() {
      return {
        slide: 0,
        sliding: null,
      }
    },
    methods: {
      onSlideStart(slide) {
        this.sliding = true
      },
      onSlideEnd(slide) {
        this.sliding = false
      },
      linkmenu: function(){
        location.href="foodmenu"
      },
      linkcontact: function(){
        location.href="contact"
      }

    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import url('https://fonts.googleapis.com/css?family=Courgette|Open+Sans&display=swap');
.container-body{
    margin-top: 100.5px;
}
h1{
    /* position: block; */
    text-align: center;
    padding: 20px 20px;
    font-family: 'Courgette', cursive, sans-serif;
    font-size: 42px;

}
.brand{
    text-align: center;
    padding: 20px 20px;
    font-family: 'Courgette', cursive, sans-serif;
    font-size: 36px;
}
.location{
    text-align: center;
    padding: 0 20px;
    font-family: 'Open Sans', sans-serif;
    font-size: 18px;

}
.phone{
    text-align: center;
    padding: 20px 20px;
    color: rgb(199, 0, 0);
    font-family: 'Open Sans', sans-serif;
    font-size: 22px;
}

h2{
    /* position: block; */
    text-align: center;
    padding-top: 25px;
    padding-bottom: 10px;
    font-family: 'Open Sans', sans-serif;
    color: rgb(199, 0, 0);

}

.button{
    text-align: center;
    padding-bottom: 15px;
}
.btn{
    padding: 0.375rem 2rem;

}
.carousel-con{
    padding: 3% 10%;
}
h4{
    padding: 10px 20px;
    text-align: center;
    font-size: 32px;
    font-family: 'Courgette', sans-serif;
}
.table-con{
    padding: 10px 20px;
    text-align: center; 
    font-size: 20px;   
}

td{
    padding: 0 6px;
}
.btn-caro{
    text-decoration: none;
    background-color: rgb(199, 0, 0);
    color: rgb(255, 255, 255);
    border: 1px solid transparent;
    border-color: rgb(0, 0, 0);
    border-radius: 5px;
    padding: 5px 15px;
}

.btn-caro:hover{
    opacity: .7;
}
@media (max-width: 850px){
    h1{
        font-size: 34px;
    }
    h2{
        font-size: 26px;
    }
    .blank-img{
        font-size: 14px;
    }
    .table-con{
        font-size: 18px;
    }
}

</style>
