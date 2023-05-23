<script>
import AppBlueSection from './AppBlueSection.vue'
  export default {
    name: "AppMain",
    props:{
      arrayCard:Array,
    },
    components:{
        AppBlueSection
    },
    data() {
      return {
     
      }
    },
    methods: {
        
    },
    mounted() {
   
    }
  }
</script>

<template>
  <main>
  
    <div class="container bg-dark">
      <div class="row  text-light">
        <!--foto grande jumbotron-->    
        <div class="col-12 my-height"></div>
        <!--inizio slide titolo-->
        <div class="col-3 rounded">
          <h4 class="m-2" >CURRENT SLIDE</h4>
        </div>
        
       
        <div class="d-flex flex-wrap col-10 mx-auto">
          <!--dinamico preso da app.Vue-->
          <template v-for="oggetto in arrayCard">   
            <div class="m-4 my-card d-flex flex-column rounded">
              <div class="my-class ">
                <img class="rounded-top"  :src= oggetto.thumb alt=""> 
              </div>
              <div class="d-flex justify-content-center align-items-center">
                <p>{{ oggetto.series }}</p>
              </div>              
            </div>
          </template>
        </div>
          
       
      </div>
    </div>
        
    <AppBlueSection/>
  </main>
</template>

<style lang="scss" scoped>
  @use'../style/variabili/_variables.scss' as*;

  div{
    .my-height{
      background-image: url(../assets/jumbotron.jpg);
      background-position: top;
      background-size: cover;
      height: 300px;
    }
    div.col-3{
      background-color: $blue;
      text-align: center;
      margin: 0.5rem auto;

    }
    div.my-card{
      width: calc(100% / 6 - 3rem);
      height: 250px;
      border: 1px solid white;
      &:hover{
        cursor: pointer;
        transform: scale(1.1);
      }
      img{
      width: 100%;
      height: 100%;
      object-fit:cover;
      }
      p{
        text-align: center;
        padding-top: 5px;
        font-size: 10px;
      }
      .my-class{
      width: 100%;
      height: 200px;
    }
    }
    
    
  }
</style>