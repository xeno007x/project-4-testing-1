<template>
  <div class="about">
    <h1>This is an about page</h1>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Excepturi explicabo provident facere similique esse maxime unde. Nesciunt officiis saepe blanditiis quidem voluptatem cum alias accusantium qui aut, veniam debitis laborum? Optio velit quia beatae cupiditate dolorem sed, doloribus omnis maiores!</p>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Excepturi explicabo provident facere similique esse maxime unde. Nesciunt officiis saepe blanditiis quidem voluptatem cum alias accusantium qui aut, veniam debitis laborum? Optio velit quia beatae cupiditate dolorem sed, doloribus omnis maiores!</p>
  </div>
  <product-list-one/>
  <product-list-two/>
</template>

<script>
import ProductListOne from '@/components/ProductListOne.vue'
import ProductListTwo from '@/components/ProductListTwo.vue'

export default {
  name: 'AboutView',
  components: {
    ProductListOne,ProductListTwo,
  }
}
</script>