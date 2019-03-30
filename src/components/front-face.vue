<template>
    <div id="front_face" class="surface_1 animated zoomIn">
           <animatingSmallCircles/>
          <div id="prime-msg">
              <h1>Welcome {{user.name}}</h1>
           </div>    
           
       
        
    </div>
</template>

<script>
import animatingSmallCircles from './animating-circles'
export default {
    components:
    {
        animatingSmallCircles
    },
    props:{
        
        user:Object,
    }
}
</script>


<style scoped>
#front_face
{
    background:#000000c7;
    width: 70vh;
    height: 70vh;
    border-radius: 50%;
    margin: auto;
    display: grid;
}
#prime-msg
{
    display: grid;
}
#prime-msg h1 {
    margin: auto;
    letter-spacing: 2px;
}

</style>
