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
    <div class="container border border-dark mt-4">
      <div class="row justify-content-around">

        <!--sezione sinistra-->
        <div class="col-1">
          <a class="" href="#">
            <img :src=logo alt="Logo">
          </a>  
        </div>
        
        <!--sezione destra fatta dinamica-->
        <div class="col-7 d-flex justify-content-end align-items-center">
          <template v-for="oggetto in arrayHeaderSection" >
            <section class="p-2">
              <a>{{ oggetto.tipo }}</a>
            </section>
          </template>
        </div>

      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
  @use'../style/variabili/_variables.scss' as*;
  
  header{
    img{
      width: 4rem;
      margin: 1rem;
    } 
  }
  section{
    &:hover{
      color: $blue;
      border-bottom: 1px solid $blue;
      cursor: pointer;
    }
  }
</style>
