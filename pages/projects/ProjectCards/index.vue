<template>
  <section class="cardList">
    <Card
      v-for="CardData in cardData"
      :key="CardData.id"
      :classes="CardData.classes"
      :id="CardData.id"
      :framework="CardData.framework"
      :thumbnail="CardData.thumbnail"
      :title="CardData.title"
      :description="CardData.description"
      :subDescription="CardData.subDescription"
      :deployLink="CardData.deployLink"
      :githubLink="CardData.githubLink"
    />
  </section>
</template>

<script>
import Card from '~/components/PortfolioCards/Card'
import CardData from '~/components/Cards/CardInfo/ReactCardInfo/cardInfo.json'
export default {
  components: {
    Card,
  },
  data() {
    return {
      cardData: CardData,
      gitlink: true,
    }
  },
}
</script>

<style scoped>
.cardList {
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
</style>