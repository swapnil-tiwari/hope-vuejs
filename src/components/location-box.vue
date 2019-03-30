<template>
    <div id="location" class="surface_1">
        <span v-html="location">{{location}}</span>
    </div> 
</template>

<script>
export default {
    data()
    {
        return {
            location:'Location not Available'
        }
    },
    methods:
    {
       getLocation() {
        if (navigator.geolocation) {
            navigator.geolocation.getCurrentPosition(this.showPosition);
        } else { 
            this.location = "Location not Available";
        }
        }, showPosition(position) {
       this.location = "Latitude: " + position.coords.latitude + 
        "<br>Longitude: " + position.coords.longitude;
        }  
    },
    mounted() {
        this.getLocation();
    },
}
</script>
<style scoped>
#location
{
    width:fit-content;
    padding: 10px;
    box-sizing: border-box;
    height: 10vmin;
    position: fixed;
    top:0px;
    left:0px;
}
</style>

