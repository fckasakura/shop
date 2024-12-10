<template>
  <div class="product-list">
    <div v-for="product in products" :key="product.id" class="product-item">
      <div class="product-image">
        <img :src="product.image" :alt="product.title" />
      </div>
      <h3 class="product-title">{{ product.title }}</h3>
      <p class="product-price">${{ product.price.toFixed(2) }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      products: [
        {
          id: 1,
          title: "Classic Monochrome Tees",
          price: 35,
          image: require('@/assets/product1.png'),
          inStock: true,
        },
        {
          id: 2,
          title: "Essential Neutrals",
          price: 22,
          image: require('@/assets/product2.png'),
          inStock: true,
        },
        {
          id: 3,
          title: "UTRAANET Black",
          price: 43,
          image: require('@/assets/product3.png'),
          inStock: true,
        },
        {
          id: 4,
          title: "Elegant Ebony Sweatshirts",
          price: 35,
          image: require('@/assets/product4.png'),
          inStock: true,
        },
        {
          id: 5,
          title: "Sleek and Cozy",
          price: 57,
          image: require('@/assets/product5.png'),
          inStock: false,
        },
        {
          id: 6,
          title: "Raw Black Tees",
          price: 19,
          image: require('@/assets/product6.png'),
          inStock: true,
        },
        {
          id: 7,
          title: "MOCKUP black",
          price: 30,
          image: require('@/assets/product7.png'),
          inStock: true,
        },
        {
          id: 7,
          title: "Athletic Shirt",
          price: 35,
          image: require('@/assets/product8.png'),
          inStock: true,
        },
      ],
    };
  },
};
</script>

<style scoped>
body {
  background-color: white; 
}

.product-list {
  display: grid;
  gap: 1rem; 
  margin: 0 auto;
  padding: 1rem;
  max-width: 1200px; 
}

.product-item {
    text-align: center;
}

.product-image {
  background-color: #F6F6F6;
  padding: 0.5rem;
  border-radius: 5px;
}

.product-item img {
  max-width: 100%;
  height: auto;
  border-radius: 5px;
}

.product-title {
  font-size: 1rem; 
  font-weight: normal; 
  text-align: left; 
  margin-left: 0.5rem; 
}

.product-price {
  font-size: 0.9rem;
  font-weight: normal;
  text-align: left;
  margin-left: 0.5rem;
}

@media (min-width: 320px) {
  .product-list {
    grid-template-columns: repeat(1, 1fr);
  }
}

@media (min-width: 480px) {
  .product-list {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (min-width: 768px) {
  .product-list {
    grid-template-columns: repeat(3, 1fr);
  }
}

@media (min-width: 1024px) {
  .product-list {
    grid-template-columns: repeat(4, 1fr);
  }
}
</style>

