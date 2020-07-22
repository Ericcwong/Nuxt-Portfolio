<template>
  <section class="cardList">
    <b-card-group>
      <Card
        v-for="CardData in cardData"
        :key="CardData.id"
        :id="CardData.id"
        :framework="CardData.framework"
        :thumbnail="CardData.thumbnail"
        :title="CardData.title"
        :description="CardData.description"
        :deployLink="CardData.deployLink"
        :githubLink="CardData.githubLink"
      />
    </b-card-group>
  </section>
</template>

<script>
import Card from "~/components/PortfolioCards/Card";
import CardData from "~/components/Cards/CardInfo/ReactCardInfo/cardInfo.json";
console.log(CardData[0].framework)
export default {
  components: {
    Card
  },
  data() {
    return {
      cardData: CardData,
      gitlink: true
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
  justify-content: space-around;
}
