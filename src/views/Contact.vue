<template>
  <div class="contact">
    <navbar />
    <h1 class="page-heading">Contact</h1>

    <!-- CONTACT FORM -->
    <div class="contact-form" align="center">
    <b-form @submit="onSubmit" @reset="onReset" >
      
      <b-form-group id="input-group-2" label-for="input-2">
        <b-form-input
          id="input-2"
          v-model="form.name"
          required
          placeholder="Enter name"
        ></b-form-input>
      </b-form-group>

      <b-form-group id="input-group-3" label-for="input-2">
        <b-form-input
          id="input-3"
          v-model="form.phone"
          required
          placeholder="Phone"
        ></b-form-input>
      </b-form-group>

      <b-form-group
        id="input-group-1"
        label-for="input-1"
        description=""
      >
        <b-form-input
          id="input-1"
          v-model="form.email"
          type="email"
          required
          placeholder="Enter email"
        ></b-form-input>
      </b-form-group>

      <!-- SUBMIT AND RESET BUTTON -->
      <div class="submit-btn"><b-button type="submit" variant="primary">Submit</b-button></div>
      <div class="reset-btn"><b-button type="reset" variant="danger">Reset</b-button></div>
    </b-form>
  </div>
    <!-- BOOTSTRAP+VUE GRID -->
    <b-container class="bv-example-row">
      <b-row>
        <b-col sm="12" cols="12">
          <h4>Special Requests?</h4>
          <p class="text">Do you have any concerns? Questions about catering for an upcoming event? 
          Drop us a line, and we'll get back to you soon!</p>
        </b-col>
      </b-row>
    </b-container>  

    <b-container class="bv-example-row">
      <b-row>
        <b-col sm="6" cols="6">
          <h4 class="brand">The Square</h4>
          <p class="location">1351  Sunny Day Drive, Los Angeles, California </p>
          <p class="location">90017, United States</p>
          <p class="phone">(714)-810-4275</p>
        </b-col>
      
      
        <b-col sm="6" cols="6">
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
        </b-col>
      </b-row>
    </b-container>

    <!-- FOOTER -->
    <footerComp/>
  </div>
</template>

<script>
// @ is an alias to /src
import navbar from '@/components/navbar.vue'
import footerComp from '@/components/footerComp.vue'

export default {
  name: 'contact',
  components: {
    navbar,
    footerComp
  },

  data: function() {
    return {
      form: {
        email: '',
        name: '',
        phone: '',
      },
    }
  },

  methods: {
      onSubmit(evt) {
        evt.preventDefault()
        alert(JSON.stringify(this.form))
      },
      onReset(evt) {
        evt.preventDefault()
        // Reset our form values
        this.form.email = ''
        this.form.name = ''
        this.form.phone = ''
        // Trick to reset/clear native browser form validation state
        
      }
    }
  }
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css?family=Lato|Courgette|Open+Sans&display=swap');
  
  .contact{
    margin-top: 100.5px;
  }
  .page-heading{
    top: 0;
    bottom: 0;
    padding: 30px;
    text-align: center;
    padding-left: 40px;
    font-family: 'Courgette', sans-serif;
    font-size: 36px;
    /* color: rgb(199, 0, 0); */
  }
  .table-con{
    padding: 0 20px 20px 20px;
    text-align: center; 
    font-size: 20px;   
    color: rgb(94, 94, 94);
  }
  .brand{
    text-align: center;
    padding: 20px;
    font-family: 'Courgette', cursive, sans-serif;
    font-size: 30px;
  }
  .location{
    text-align: center;
    padding: 4px 20px;
    font-family: 'Open Sans', sans-serif;
    font-size: 18px;
    margin: 0;
    color: rgb(94, 94, 94);
  }
  .phone{
    text-align: center;
    padding: 20px;
    color: rgb(199, 0, 0);
    font-family: 'Open Sans', sans-serif;
    font-size: 22px;
    margin: 0;
  }
  h4{
    margin: 0;
    padding: 20px;
    text-align: center;
    font-size: 30px;
    font-family: 'Courgette', sans-serif;
  }
  .contact-form{
    padding: 0 20px 30px 20px;
  }
  .form-control{
    width: 55%;
    border: none;
    border-bottom: 1px solid rgba(0, 0, 0, 0.1);
    border-radius: 0;
    padding-top: 30px;
    padding-bottom: 15px;
  }
  .submit-btn{
    padding: 0 20px;
    display: inline-block;
  }
  .reset-btn{
    padding: 0 20px;
    display: inline-block;
  }
  .btn-danger{
    background-color: transparent;
    color: rgb(199, 0, 0);
  }
  .btn-primary {
    color: #007bff;
    background-color: transparent;
  }
  .btn-danger:hover{
    color: white;
    background-color: rgb(199, 0, 0);
  }
  .btn-primary:hover{
    color: white;
    background-color: #007bff;
  }
  .text{
    color: rgb(94, 94, 94);
    text-align: center;
    padding: 0 10vw 0 10vw;
  }


  @media (max-width: 850px){
    .table-con{
    padding: 0 10px 10px 10px;
    font-size: 15px;   
    }
    .col-6{
      padding: 0;
    }
    .brand{
      padding: 20px;
      font-size: 26px;
    }
    .location{
      padding: 4px 20px;
      font-size: 15px;
    }
    .phone{
      font-size: 19px;
    }
    h4{
      margin: 0;
      padding: 20px;
      text-align: center;
      font-size: 26px;
      font-family: 'Courgette', sans-serif;
    }
    .contact-form{
      padding: 0 10px 20px 10px;
    }
    .form-control{
      width: 80%;
      padding-top: 30px;
      padding-bottom: 15px;
    }
  }
</style>
