<template>
    <div class="Cards-Row">
      <Cards
        v-for="i in Cards"
        :key="i.Cards"
        :bg="i.bg"
        :Img="i.Img"
        :Text="i.Text"
        :bgBtn="i.btncolor"
        :TextBtn="i.TextBtn" />
    </div>
  </template>
  
  <script>
  import Cards from "../components/Cards.vue";
  import Buttons from "../components/Buttons.vue";
  import { useProductStore } from "../store/product";
  import { mapState } from "pinia"
  export default {
    name: "CardsProduct",
    components: {
      Cards,
      Buttons,
    },
    computed: {
      ...mapState(useProductStore, ["Cards"])
    }
  };
  </script>
  
  <style scoped>
  @import url("https://fonts.googleapis.com/css2?family=Kantumruy+Pro:ital,wght@1,300;1,400;1,500;1,600;1,700&family=Poppins:wght@300;400;500;600;800&family=Quicksand:wght@400;600;700&display=swap");
  
  .Cards-Row {
    width: 100%;
    display: flex;
    justify-content: start;
    align-items: center;
    gap: 15px;
  }
  </style>