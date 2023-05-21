<script>
    import AppMiniFooter from './AppMiniFooter.vue'
  export default {
    name: "AppFooter",
    components:{
        AppMiniFooter
    },
    data() {
      return {
        ArraySectionFooter:[
            {
                title:"DC COMICS",
                listFooter:[
                    "Charactes",
                    "Comics",
                    "Movies",
                    "TV",
                    "Games",
                    "Videos",
                    "News",
                ]
            },
            {
                title:"DC",
                listFooter:[
                    "Terms Of Use",
                    "Privacy politicy (New)",
                    "Ad Choices",
                    "Advertising",
                    "Jobs",
                    "Subscriptions",
                    "Talent Workshops",
                    "CPSC Certificates",
                    "Ratings",
                    "Shop Help",
                    "Contact Us",
                ]
            },
            {
                title:"SITES",
                listFooter:[
                    "DC",
                    "MAD Magazine",
                    "DC Kids",
                    "DC Universe",
                    "DC Power Visa",
                ]
            },
            {
                title:"SHOP",
                listFooter:[
                    "Shop DC",
                    "Shop DC Collectibles"
                ]
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
  <footer>
    <section class="container">
        <div class="row text-light align-self-stretch ">
            <div class="col-6 d-flex justify-content-around">
                <div class="d-flex flex-wrap">

                    <!--footer maxi fatto in maniera dinamica-->
                    <template v-for="oggetto in ArraySectionFooter">
                        <div class="col-4">
                            <p class="mt-2">{{ oggetto.title}}</p>
                            <ul>
                                <li class="text-secondary" v-for="oggetto in oggetto.listFooter">{{ oggetto }}</li>
                            </ul>
                        </div>
                    </template>
                    
                </div>
            </div>
            <div class="col-6 d-flex justify-content-center my-bg"></div>
        </div>
    </section>
    
    <AppMiniFooter/>
  </footer>
  
  
</template>

<style scoped>
    section{
        background-image: url(../assets/footer-bg.jpg);
        
        background-size: cover;
    }
   img{
    width: 200px;
   }
   p{
    cursor: pointer;
   }
    ul{
        list-style-type: none;
        padding: 0;
        cursor: pointer;
        font-size: 10px;
    }
    li:hover{
        color: white !important;
    }
    .my-bg{
        background-image: url(../assets/dc-logo-bg.png);
        background-position: center;
        background-repeat: no-repeat;
    }
</style>
