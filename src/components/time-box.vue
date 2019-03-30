<template>
    <div id='timeBox' class="surface_1">
        Date : <span v-html="date"></span>
    </div>   
</template>
<script>
const months=['January','February','March','April','May','June','July','August','September','October','November','December']
let today=new Date();
    let date=today.getDate()+ '&nbsp' + months[(today.getMonth())] + '&nbsp' + today.getFullYear();
    //let time=today.getHours()+ ' : ' + today.getMinutes();
export default {

    data()
    {
        return {
            date: date,
        }
    }
}
</script>

<style scoped>
#timeBox
{
    width:fit-content;
    padding: 10px;
    box-sizing: border-box;
    height: 10vmin;
    position: fixed;
    top:0px;
    right:0px;
}
</style>

