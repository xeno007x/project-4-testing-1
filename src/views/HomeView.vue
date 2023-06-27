<template>
  <div class="home">
    <H1>Namaste, Welcome to Home Page</H1>
    <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Laborum odit hic distinctio numquam cum autem quis et natus? Beatae, neque. Asperiores ipsum dignissimos sequi illum inventore odio perspiciatis doloribus repudiandae corrupti animi. Doloremque aspernatur provident, veritatis minima omnis expedita? Iusto!</p>
  </div>
  <product-list-one/>
  

</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import ProductListOne from '@/components/ProductListOne.vue'
import ProductListTwo from '@/components/ProductListTwo.vue'


export default {
  name: 'HomeView',
  components: {
    HelloWorld,ProductListOne
  }
}
</script>
