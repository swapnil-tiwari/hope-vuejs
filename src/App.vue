<template>
  <div id="app">
    <div class="background">
    </div>
    <div class="overlay"></div>
    <div class="main-cont">
      <frontFace :user="{name:'Swapnil'}">
        
      </frontFace> 
    </div> 
    
  </div>
</template>

<script>
import frontFace from './components/front-face'
export default {
  name: 'App',
  components: {
    frontFace,
    
  }
}
</script>

<style>
@import url(assets/css/style.css);
@import url('https://fonts.googleapis.com/css?family=Raleway');

#app {
  font-family: 'Raleway', sans-serif;
  font-weight: unset;
  text-align: center;
  color: #fff;
}

</style>
