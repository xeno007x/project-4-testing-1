<template>
    <div id="product-list-one">
        <h2>Product List One</h2>
        <ul>
            <li v-for="product in saleProducts" :key="product.name">
                <span class="name">{{ product.name }}</span>
                <span class="price">₹{{ product.price }}</span>
            </li>
        </ul>
        
            <label for="payload">Reduce Price By:</label>
            <input type="number" id="payload" v-model="inputAmount" />
            <button @click="reducePrice">Reduce Prices</button>
        
        <h1>{{ inputAmount }}</h1>
    </div>
</template>

<script>


export default {
    data() {
      return {
        inputAmount: 0
      };
    },
    computed: {
        products(){
            return this.$store.state.products;
        },
        saleProducts(){
            return this.$store.getters.saleProducts;
        }
    },
    methods:{
    reducePrice() {
      const payload = parseInt(this.inputAmount);
      if (!isNaN(payload)) {
        this.$store.dispatch('reducePrice', payload);
      }
    }
  } 
}
    
    
    
        //{
       

        // reducePrice: function(payload){
            // this.$store.commit('reducePrice', amount);

            
            // this.$store.dispatch('reducePrice', payload);
    //     }
    // }

</script>

<style scoped>
#product-list-one {
  background: #FFF8B1;
  box-shadow: 1px 2px 3px rgba(0, 0, 0, 0.2);
  margin-bottom: 30px;
  padding: 10px 20px;
}

#product-list-one ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

#product-list-one li {
  display: inline-block;
  margin-right: 10px;
  margin-top: 10px;
  padding: 20px;
  background: rgba(255, 255, 255, 0.7);
  border-radius: 5px;
  transition: background-color 0.3s;
}

#product-list-one li:hover {
  background-color: rgba(255, 255, 255, 0.9);
}

.price {
  font-weight: bold;
  color: #E8800C;
}
</style>
