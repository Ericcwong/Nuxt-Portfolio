<template>
  <section class="cardList">
    <Card
      v-for="CardData in cardData"
      :key="CardData.id"
      :id="CardData.id"
      :thumbnail="CardData.thumbnail"
      :title="CardData.title"
      :description="CardData.description"
    />
  </section>
</template>

<script>
import Card from "~/components/Cards/Card";
import CardData from "./CardInfo/cardInfo.json";
export default {
  components: {
    Card
  },
  data() {
    return {
      cardData: CardData
    };
  }
};
</script>

<style scoped>
.cardList {
  width: 100%;
  display: flex;
  padding: 20px;
  flex-wrap: wrap;
}
</style>