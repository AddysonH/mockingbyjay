<template>
<div>
    <div class="row navMargin">
        <div class="col-12 ">
                <NavBarComp />
        </div>  
      </div>
      <div class="row navMargin">
          <div class="col-12 recordTop">
                <CarouselComponent />
          </div>  
      </div>
      <div class="row navMargin">
          <div class="col-12">     
                <SideCover/>
          </div> 
      </div>
      <div class="row navMargin">
          <div class="col-12">     
                <SideLine />
          </div> 
      </div>
  </div>
</template>

<script>
// @ is an alias to /src
import CarouselComponent from "../components/CarouselComponent.vue"
import SideLine from "../components/SideLine.vue"
import SideCover from "../components/SideCover.vue"
import NavBarComp from "../components/NavBarComp.vue"
export default {
  name: 'Home',
  components: {
    CarouselComponent,
    SideLine,
    SideCover,
    NavBarComp
  }
}
</script>
<style >

body{
  margin:0;
}

.recordTop{
  margin-top: 110px;
  overflow: hidden;
  z-index: 1;
}

.navMargin{
  margin:0;
}
.marginLine{
  margin-bottom: 1q00px;
}





</style>
