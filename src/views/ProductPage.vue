<template>
    <div class="Product-Row">
      <Products
        v-for="i in Products"
        :key="i.Products"
        :bg="i.bg"
        :ItemName="i.ItemName"
        :Img="i.Img"
        :ItemNumber="i.ItemNumber">
      </Products>
    </div>
  </template>
  
  <script>

  import Products from "../components/Products.vue";
  import { useProductStore } from "../store/product";
  import { mapState } from "pinia"
  export default {
    name: "ProductPage",
    components: {
      Products,
    },

    computed: {
      ...mapState(useProductStore, ["Products"])
    }
  };
  </script>
  
  <style>
  @import url("https://fonts.googleapis.com/css2?family=Kantumruy+Pro:ital,wght@1,300;1,400;1,500;1,600;1,700&family=Poppins:wght@300;400;500;600;800&family=Quicksand:wght@400;600;700&display=swap");
  
  .Product-Row {
    margin-top: 30px;
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  </style>
  <!-- Width
  1586px
  Height
  185px -->