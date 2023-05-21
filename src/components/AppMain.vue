<script>
import AppBlueSection from './AppBlueSection.vue'
  export default {
    name: "AppMain",
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
      <!--container nero-->
        <div class="container bg-dark">
            <div class="row  text-light">
                <p class="m-2 p-4" >Content here </p>
            </div>
        </div>
        
        <AppBlueSection/>
    </main>
</template>

<style scoped>

</style>