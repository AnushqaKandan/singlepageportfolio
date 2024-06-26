<template>
  <div class="container">
    <div class="row">
     <div class="col">
        <img src="https://anushqakandan.github.io/All-images/Images/AnushiPro.JPG " alt="profile" class="img-fluid" loading="lazy">
     </div>

     <div class="col"> 
        <div id="details">
           <h1 class="display-1">Anushqa Kandan</h1>
           <span> {{ jobTitle }}</span>
        </div> 
     </div>
    </div>
  </div>
</template>

<script setup>
import{ computed, onMounted } from 'vue'
const jobTitle = 
computed(() => this.$store.state.jobTtle)
onMounted(() => { this.$store.dispatch('fetchJobTitle')

})

</script>

<style>

</style>