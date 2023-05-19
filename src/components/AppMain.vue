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
      console.log("main")
    }
  }
</script>

<template>
    <main>
        <h1 class="text-center">ciao</h1>
        <AppBlueSection/>
    </main>
</template>

<style scoped>

</style>