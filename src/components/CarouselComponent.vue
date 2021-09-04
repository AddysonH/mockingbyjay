<template>
<div class="wheel">
    <div class="card">{{carousel}}</div>
    <div class="card">{{carousel}}</div>
    <div class="card">{{carousel}}</div>
    <div class="card">{{carousel}}</div>
    <div class="card">{{carousel}}</div>
    <div class="card">{{carousel}}</div>
    <div class="card">{{carousel}}</div>
    <div class="card">{{carousel}}</div>

</div>
</template>
<script>

export default ({
   name:"CarouselComponent",
  
   data(){
       
       return{
         
       }
   },
   computed:{


   }, 
   methods:{
       
   
   },
   mounted(){
       let theta = Math.PI / 4.0;
       let new_theta = 0.0;
       let new_x = 0.0;
       let new_y = 0.0;
       let wheel_radius = 200.00;
       const cards = document.querySelectorAll('.card');
       const center = {
        x: parseFloat(getComputedStyle(cards[0]).left),
        y: parseFloat(getComputedStyle(cards[0]).top)
    }

    cards.forEach((card, index) => {
        new_theta = theta * index;
        new_x = (Math.cos(new_theta) * wheel_radius);
        new_y = (-1.0 * Math.sin(new_theta) * wheel_radius);

        card.style.left = `${center.x + new_x}px`;
        card.style.top = `${center.y + new_y}px`;
    });

    
   }
   
})
</script>

<style>
.wheel {
    width: 300px;
    height: 200px;
    background-color: blue;

/* This is based off the top left corner of the rectangle. It is placed in the center of the page. */
    position: absolute;
    left: 50%;
    top: 50%;
    /* This moves the whole square to the center of the page */
    /* This is the wheel. Wherever this moves the images move */
    transform: translate(-50%, -50%);
}
.card {
    width: 90px;
    height: 50px;
    background-color: red;

    position: absolute;
    top:50%;
    left:50%;
    transform: translate(-50%,-50%);

}
</style>
