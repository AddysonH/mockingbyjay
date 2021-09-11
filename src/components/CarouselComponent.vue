<template>
<div class="center">
<div class="record"></div>
<div class="wheel ">
    <div class="card circle"><img class="circle" src="https://place-hold.it/100x100"></div>
    <div class="card circle"><img class="circle" src="https://place-hold.it/100x100"></div>
    <div class="card circle"><img class="circle" src="https://place-hold.it/100x100"></div>
    <div class="card circle"><img class="circle" src="https://place-hold.it/100x100"></div>
    <div class="card circle"><img class="circle" src="https://place-hold.it/100x100"></div>
    <div class="card circle"><img class="circle" src="https://place-hold.it/100x100"></div>
    <div class="card circle"><img class="circle" src="https://place-hold.it/100x100"></div>
    <div class="card circle"><img class="circle" src="https://place-hold.it/100x100"></div>
</div>
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
       let wheel_radius = 300.00;
       let wheel_theta = 0;
       const cards = document.querySelectorAll('.card');
       const wheel = document.querySelector('.wheel');
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

       

       document.addEventListener('wheel', event => {
           let scroll_speed = event.wheelDeltaY + 0.002;
           wheel_theta = wheel_theta + scroll_speed;
            wheel.style.transform = `translate(-50%, -50%) rotate(${wheel_theta + (180/Math.PI)}deg)`       })
     

   }

    
   
})
</script>

<style>
.wheel {
    width: 300px;
    height: 200px;
    /* background-color: blue; */
    margin-top: 50px; 
/* This is based off the top left corner of the rectangle. It is placed in the center of the page. */
    position: absolute;
    left: 50%;
    top: 50%;
    /* This moves the whole square to the center of the page */
    /* This is the wheel. Wherever this moves the images move */
    transform: translate(-50%, -50%);
}
.card {
    width: 100px;
    height: 100px;
    background-color: rgb(184, 184, 184);

    position: absolute;
    top:50%;
    left:50%;
    transform: translate(-50%,-50%);

}
.center{
display: flex;
justify-content: center;
align-items: center;
}

.circle{
    border-radius:50%;
    display: inline-block;
    margin-right:20px;
}
.record{
    width:1300px;
    height:1300px;
    background-image: url("../assets/brett-jordan-hrUhyFq6u-A-unsplash.png");
    background-size: 800px 800px;
    background-repeat: no-repeat;
    margin-top: 50px; 

    /* width: 300px;
    height: 200px;     */

/* This is based off the top left corner of the rectangle. It is placed in the center of the page. */
    position: absolute;
    left: 50%;
    top: 50%;
    /* This moves the whole square to the center of the page */
    /* This is the wheel. Wherever this moves the images move */
    transform: translate(-30%, -30%);
}
</style>
