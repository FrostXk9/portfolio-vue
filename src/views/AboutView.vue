<template>
    
  <div v-for="ix of $store.state.aboutData">
    <!-- <div class="container col-xxl-8 px-4 py-5"> -->
    <div class="container col-xxl-12 px-3 py-5">

      <div class="row flex-lg-row align-items-center g-5 py-5">

        <div class="col-10 col-sm-12 col-lg-6" id="imgContainer">

          <img :src="ix.myImage" class="d-block mx-lg-auto img-fluid" :alt="ix.imgAlt" id="imge" loading="lazy">

        </div>

        <div class="col-lg-6">

          <h1 class="display-5 fw-bold lh-1 mb-3 text-white">{{ ix.topText }}</h1>

          <p class="lead text-white-50 text-center" id="txt">{{ ix.pText }}</p>

          <div class="d-grid gap-2 d-md-flex justify-content-md-center">

            <button type="button" class="btn btn-outline-primary btn-lg px-4">Default</button>

          </div>
              
        </div>

      </div>
      <!-- <div id="card"></div> -->
      
      <div class="" id="expBox">
        <img :src="ix.html5" alt="" id="card" data-v-img>

        <img :src="ix.css" alt="" id="card" data-v-img>

        <img :src="ix.Bootstrap" alt="" id="card" data-v-img>

        <img :src="ix.JavaScript" alt="" id="card" data-v-img>
        
        <img :src="ix.NodeJs" alt="" id="card" data-v-img>
        
        <img :src="ix.ReactJS" alt="" id="card">
        
        <img :src="ix.Redux" alt="" id="card">
        
        <img :src="ix.Python" alt="" id="card">
        
        <img :src="ix.ReactBootstrap" alt="" id="card">
        
        <img :src="ix.Cpp" alt="" id="card">
        
        <img :src="ix.VueJs" alt="" id="card">
        
        <img :src="ix.VueX" alt=""  id="card">
      </div>
    </div>



  </div>

</template>
<script>
export default {
  components : {

  },
  methods : {
    fetchAboutData : function(){
      this.$store.dispatch('fetchAboutData')
    }
  },
  mounted(){
    this.fetchAboutData()
  }
}
</script>
<style>
/* *{
  overflow: hidden;
} */

#imge{
  height: 397px;
  transition: all 1s ease-in-out;
}

#txt{
  overflow: scroll;
  max-height: 270px;
}

::-webkit-scrollbar {
  width: 10px;
}

/* Track */
::-webkit-scrollbar-track {
  -webkit-border-radius: 10px;
  scroll-behavior: smooth;
  border-radius: 5px;
}

::-webkit-scrollbar-corner{
  background-color: rgba(0, 255, 255, 0);
}

::-webkit-scrollbar-thumb {
  -webkit-border-radius: 10px;
  border-radius: 10px;
  background: rgba(255, 255, 255, 0); 
}

/* triggers when page is inactive */
::-webkit-scrollbar-thumb:window-inactive {
  background: rgba(95, 95, 95, 0); 
}

#card {
  width: 50px;
  height: 50px;
  padding: 5px;
  margin-left: 5px;
  border-radius: 50%;
  background: #e0e0e0;
  /* filter: grayscale(50%); */
  box-shadow: 15px 15px 30px #fffffffd inset,-5px -5px 30px #ffffff27;
}

/* #expBox{
  min-height: 20vh;
} */

@media (max-width: 780px){
  #imge{
    height: 290px;
  }
  
  #txt{
    overflow: scroll;
    max-height: 170px;
    font-size: 15px;
  }
}

@media (max-width: 501px) {
  #imgContainer{
    display: flex;
    justify-content: center;
  }
  ::-webkit-scrollbar {
   width: 6px;
  }
}
  
</style>