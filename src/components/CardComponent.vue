<template>
  <article>
    <header>
      {{cardData.header}}, {{cardData.age}}+
    </header>
    <div class="info">
      <div class="type">{{cardData.type}}</div>
      <div class="playerCount">для {{cardData.playerCount}} человек</div>
      <div class="location">{{cardData.location}}</div>
      <div class="difficulty">сложность {{cardData.difficulty}}/10</div>
    </div>
    <div class="description">
      {{cardData.description}}
    </div>
  </article>
  <div class="gradient"></div>
  <img src="@/assets/CardComponent/image.svg">
  <div class="white"></div>
  <div class="mostPopular">самый популярный</div>
</template>

<script>
export default {
  name: "CardComponent",
  data(){
    return{
      cardData: {
        header: "Стрелы Амура",
        age: 18,
        type: "квест",
        playerCount: 2,
        location: "для дома",
        difficulty: 7,
        description: "Романтический квест по поиску подарка для второй половинки: мужа, жены, парня или девушки. Чтобы собрать 7 стрел бога любви Амура и разыскать подарок, игроку нужно выполнить задания древних богов."
      }
    }
  }
}
</script>

<style scoped lang="scss">
  *{
    width: 831px;

  }
  .white{
    position: absolute;
    width: 344px;
    height: 361px;
    z-index: -2;
    top: 160px;
    background: #fff;
    border: transparent 0px;
    border-radius: 6px;
  }
  article{
    background: transparent;
    height: 361px;

    border-radius: 6px;
    border: transparent 0 solid;
    width: max-content;
    padding: 10px 0 0 20px;

  }
  img{
    width: 510px;
    height: 361px;
    position: absolute;
    top: 160px;
    left: 503px;
    z-index: -2;
  }

  .mostPopular{
    color: #383838;
    background: rgba(255, 255, 255, 0.8);
    border: transparent 0;
    border-radius: 4px;
    font-size: 10px;
    width: max-content;
    padding: 2px 10px;
    position: absolute;
    top: 170px;
    left: 882px;
  }

  header{
    font-size: 36px;
    font-weight: 800;
    z-index: 4;
    color: #424242;
    margin-bottom: 15px;
    width: max-content;
  }
  .info {
    width: 305px;
    height: 76px;
    display: flex;
    flex-wrap: wrap;
    margin-bottom: 13px;
    >div{
      font-size: 14px;
      padding: 4px 12px;
      background: rgba(28, 28, 28, 0.05);
      border-radius: 3px;
      margin: 3px;
      font-weight: 600;
      width: max-content;
      height: 29px;
      color: #383838;
    }
  }
  .description {
    width: 279px;
    font-size: 16px;
    color: #424242;
  }
  .gradient{
    width: 310px;
    height: 361px;
    background: rgb(255,255,255);
    background: linear-gradient(90deg, rgba(255,255,255,1) 0%, rgba(255,255,255,0) 100%);
    position: absolute;
    z-index: -1;
    top: 160px;
    left: 503px;

  }
</style>
