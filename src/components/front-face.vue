<template>
    <div id="front_face" class="surface_1 animated zoomIn">
           <animatingSmallCircles/>
          <div id="primeMsg">
              <h1>Welcome {{user.name}}</h1>
           </div>    
           
       
        
    </div>
</template>

<script>
function textToSpeech()
{
    let text=primeMsg.innerText;
    let msg = new SpeechSynthesisUtterance(text);
    window.speechSynthesis.speak(msg);
    console.log('Called');
}
import animatingSmallCircles from './animating-circles'
export default {
    components:
    {
        animatingSmallCircles
    },
    props:{
        
        user:Object,
    },
    mounted()
    {
        textToSpeech();
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
#primeMsg
{
    font-size: 2vmin;
    display: grid;
    text-align:center
}
#primeMsg h1 {
    margin: auto;
    letter-spacing: 2px;
}
@media only screen and (max-width: 480px) {
    #front_face
    {
        width: 50vh;
        height: 50vh;
    }
  }


</style>
