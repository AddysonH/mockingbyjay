<template>
  <div class="home">
   <CarouselComponent/>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import CarouselComponent from "../components/CarouselComponent.vue"

export default {
  name: 'Home',
  components: {
    HelloWorld,
    CarouselComponent
  }
}
</script>
