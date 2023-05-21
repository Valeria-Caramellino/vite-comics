<script>
  export default {
    name: "AppBlueSection",
    data() {
      return {
        ArraySectionBlu:[
            {
                icon:"src/assets/buy-comics-digital-comics.png",
                text:"DIGITAL COMICS"
            },
            {
                icon:"src/assets/buy-comics-merchandise.png",
                text:"DC MERCHANDISE"
            },
            {
                icon:"src/assets/buy-comics-subscriptions.png",
                text:"SUBSCRIPTION"
            },
            {
                icon:"src/assets/buy-comics-shop-locator.png",
                text:"COMIC SHOP LOCATOR"
            },
            {
                icon:"src/assets/buy-dc-power-visa.svg",
                text:"DC POWER VISA"
            },
        ]
      }
    },
    methods: {
        
    },
    mounted() {
  
    }
  }
</script>

<template>

    <section class="container bg-primary">

        <div class="row text-light justify-content-center p-4">
            
            <!--sezione blu fatta in maniera dinamica-->
            <template v-for="oggetto in ArraySectionBlu">
                <section class="d-flex align-items-center col-2 p-2 hover">
                    <img class="col-2" :src= oggetto.icon alt="icon">
                    <p class="col mt-3">{{  oggetto.text }}</p>
                </section>
            </template>

        </div>
    </section>
</template>

<style scoped>
    p{
        font-size: 10px;
    }
    img{
        margin: 0 1rem;
    }
    section.hover:hover{
        border-bottom: 0.5px solid white;
        cursor: pointer;
    }
</style>