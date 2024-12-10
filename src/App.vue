name: 'App',<template>
  <div id="app">
    <AppHeader />
    <main>
      <ProductList />
    </main>
    <AppFooter />
  </div>
</template>

<script>
import AppHeader from './components/Header.vue'
import AppFooter from './components/Footer.vue'
import ProductList from "./components/ProductList.vue";

export default {
  components: {
    AppHeader,
    AppFooter,
    ProductList,
  },
};
</script>

<style>
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background-color: white;
}

main {
  padding: 2rem;
}
</style>
