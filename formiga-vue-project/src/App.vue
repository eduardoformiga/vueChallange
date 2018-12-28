<template>
  <div id="app">
    
    <MyCard v-for="product in products" :cardState="product.productState">
      <template slot="header">
        <b>{{product.title}}</b>
      </template>
      <img :src="product.img">
      <p>
        <b>{{product.price}}</b>
      </p>
      <p>{{product.description}}</p>
      <template slot="footer">
        <span>Mais Detalhes</span>
      </template>
    </MyCard>
  
  </div>
</template>

<script>
import MyCard from "./components/MyCard.vue";

export default {
  name: "app",
  data() {
    return {
      products: Array
    };
  },
  mounted() {
    this.products = [
      {
        title: "Celular Xpto",
        img: "https://picsum.photos/150/150?image=0",
        price: "R$ 1.000",
        description: "Celular Lindão",
        productState: "normal"
      },
      {
        title: "PC Xpto",
        img: "https://picsum.photos/150/150?image=1",
        price: "R$ 2.000",
        description: "PC Lindão I",
        productState: "promotion"
      },
      {
        title: "PC Xyz",
        img: "https://picsum.photos/150/150?image=2",
        price: "R$ 2.500",
        description: "PC Lindão II",
        productState: "normal"
      },
      {
        title: "PC Xyz",
        img: "https://picsum.photos/150/150?image=3",
        price: "R$ 2.200",
        description: "PC Lindão III",
        productState: "normal"
      },
      {
        title: "PC Xyz",
        img: "https://picsum.photos/150/150?image=4",
        price: "R$ 2.800",
        description: "PC Lindão IV",
        productState: "promotion"
      }
    ];
  },
  components: {
    MyCard
  }
};
</script>

<style>
html {
  margin: 0;
  background-color: #f2f2f2;
}
#app {
  display: flex;
  justify-content: flex-start;
}
</style>
