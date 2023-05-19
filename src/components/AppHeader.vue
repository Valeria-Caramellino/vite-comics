<script>
  export default {
    name: "AppHeader",
    data() {
      return {
        logo: "src/assets/dc-logo.png" ,
        arrayHeaderSection:[
          {
            tipo: "CHARACTERS"
          },
          {
            tipo: "COMICS"
          },
          {
            tipo: "MOVIE"
          },
          {
            tipo: "TV"
          },
          {
            tipo: "GAMES"
          },
          {
            tipo: "COLLECTIBLES"
          },
          {
            tipo: "VIDEO"
          },
          {
            tipo: "FANS"
          },
          {
            tipo: "NEWS"
          },
          {
            tipo: "SHOP"
          },
        ]
      }
    }
  }
</script>

<template>
  <header>
    <div class="container-fluid">
      <div class="row justify-content-between">

        <!--sezione sinistra-->
        <div class="col-2">
          <a class="" href="#">
            <img :src=logo alt="Logo">
          </a>  
        </div>
        
        <!--sezione destra fatta dinamica-->
        <div class="col-10 d-flex justify-content-end align-items-center">
          <template v-for="oggetto in arrayHeaderSection" >
            <section class="p-2">
              {{ oggetto.tipo }}
            </section>
          </template>
        </div>

      </div>
    </div>
  </header>
</template>

<style scoped>
  img{
    width: 2rem;
    margin: 1rem;
  }
  section:hover{
    color: blue;
    border-bottom: 1px solid blue;
    cursor: pointer;
  }
</style>
