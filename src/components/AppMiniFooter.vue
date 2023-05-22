<script>
export default{
    name: "AppMiniFooter",
    data(){
        return{
            ArrayMiniFooter:[
                {
                    social:"src/assets/footer-facebook.png"
                },
                {
                    social:"src/assets/footer-twitter.png"
                },
                {
                    social:"src/assets/footer-youtube.png"
                },
                {
                    social:"src/assets/footer-pinterest.png"
                },
                {
                    social:"src/assets/footer-periscope.png"
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
    <section class="container ">

        <div class="row justify-content-around align-items-baseline bg-dark">
            <!--parte sinistra-->
            <div class="col-2">
                <button class="btn-outline-primary btn btn-dark text-light m-2">SIGN-UP NOW!</button>
            </div>
            <!--parte destra-->
            <div class="col-6 d-flex justify-content-end align-items-baseline">
                <p class="text-primary">FOLLOWS US</p>
                <!--dinamica con icone social-->
                <template v-for="oggetto in ArrayMiniFooter">
                    <div class=" mx-2"> 
                        <img :src= oggetto.social>
                    </div>
                </template>
            </div>
        </div>

    </section>
</template>


<style lang="scss" scoped>
    div{
        img{
            cursor: pointer;
        }
    }
</style>