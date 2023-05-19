<script>
    import AppMiniFooter from './AppMiniFooter.vue'
  export default {
    name: "AppFooter",
    components:{
        AppMiniFooter
    },
    data() {
      return {
        img:"src/assets/dc-logo-bg.png",
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
                title:"SHOP",
                listFooter:[
                    "Shop DC",
                    "Shop DC Collectibles"
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
        ]
      }
    },
    methods: {
        
    },
    mounted() {
      console.log(this.ArraySectionFooter[0].listFooter)
    }
  }
</script>

<template>
  <footer>
    <section class="container">
        <div class="row text-light ">
            <div class="col-6 d-flex justify-content-around">
                <div class="d-flex flex-column">
                    
                    <div>
                        <h2 class="mt-2">{{ ArraySectionFooter[0].title}}</h2>
                        <ul>
                            <li class="text-secondary" v-for="oggetto in ArraySectionFooter[0].listFooter">{{ oggetto }}</li>
                        </ul>
                    </div>
                    <div>
                        <h2 class="mt-2">{{ ArraySectionFooter[1].title }}</h2>
                        <ul>
                            <li class="text-secondary" v-for="oggetto in ArraySectionFooter[1].listFooter">{{ oggetto }}</li>
                        </ul>
                    </div>
                    
                </div>
                
                <div>
                    <h2 class="mt-2">{{ ArraySectionFooter[2].title }}</h2>
                    <ul>
                        <li class="text-secondary" v-for="oggetto in ArraySectionFooter[2].listFooter">{{ oggetto }}</li>
                    </ul>
                </div>
                <div>
                    <h2 class="mt-2">{{ ArraySectionFooter[3].title }}</h2>
                    <ul>
                        <li class="text-secondary" v-for="oggetto in ArraySectionFooter[3].listFooter">{{ oggetto }}</li>
                    </ul>
                </div>
                
            </div>
        
            <div class="col-6 d-flex justify-content-center">
                <img :src=img alt="logo">
            </div>
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
    ul{
        list-style-type: none;
        padding: 0;
        cursor: pointer;
    }
</style>