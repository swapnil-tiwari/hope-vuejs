<template>
  <div id="app">
    <div class="background">
    </div>
    <div class="overlay"></div>
    <div class="main-cont">
      <locationBox/>
      <timeBox/>
      <frontFace :user="{name:'Swapnil'}"/>
        
    </div> 
    
  </div>
</template>

<script>
import frontFace from './components/front-face'
import locationBox from './components/location-box'
import timeBox from './components/time-box'
export default {
  name: 'App',
  components: {
    frontFace,
    locationBox,
    timeBox
    
  },
  
}
</script>

<style>
@import url(assets/css/style.css);
@import url('https://fonts.googleapis.com/css?family=Raleway');

#app {
  font-family: 'Raleway', sans-serif;
  font-weight: unset;
  color: #fff;
}

</style>
