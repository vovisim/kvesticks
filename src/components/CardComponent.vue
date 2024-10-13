<template>
  <div class="CardComponent">
    <div class="position-relative CardComponentIns ">
      <article>
        <header>
          {{cardData.header}}, {{cardData.age}}+
        </header>

  <!--      TODO Сделать спомощью v-for-->
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
      <div class="bg-custom-cont comp">
        <div class="bg-custom">
          <div class="white"></div>
          <div class="gradient"></div>
          <img class="compImg" src="@/assets/CardComponent/image.svg">
          <div class="mostPopular">самый популярный</div>
        </div>
      </div>
      <div class="bg-custom-cont mobile">
        <div class="bg-custom">
          <img class="mobileImg" src="@/assets/CardComponent/coverMobile.svg">
          <div class="gradient"></div>
          <div class="white"></div>
          <div class="mostPopular">самый популярный</div>
        </div>
      </div>

    </div>
  </div>
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
  @media (max-width: 627px) {
    .CardComponent {
      width: 100%;
      display: flex;
      flex-direction: column;
    }

    .bg-custom-cont{
      position: absolute;
      top: 0;
      z-index: -1;
      width: 100%;
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
      top: 6px;
      left: 6px;
    }

    .CardComponentIns{
      width: 100%;
    }
    .bg-custom {
      position: relative;
      display: flex;
      flex-direction: column;
      > .white {
        width: 100%;
        height: 288px;
        background: #fff;
        border: transparent 0;
        border-radius: 6px 0 0 6px;

      }

      > .gradient {
        width: 360px;
        height: 300px;
        background: rgb(255, 255, 255);
        background: linear-gradient(0deg, rgba(255, 255, 255, 1) 0%, rgba(255, 255, 255, 0) 100%);
        z-index: 1;
        //position: absolute;
        top: 0;

      }

      > img {
        width: 100% !important;
        height: auto;
        position: absolute;
        left: 0;
        top: 0;
        border-radius: 0;
        border: transparent 0;
        overflow-x: hidden;
      }


    }
    header{
      font-size: 28px;
      font-weight: 800;
      z-index: 4;
      color: #424242;
      width: max-content;
      height: max-content;
      line-height: 120%;
    }
    article{
      padding: 0 12px;
      margin-top: 300px;
      display: flex;
      flex-direction: column;
      align-items: center;
      width: 100%;
      gap: 18px;
    }
    .comp{
      display: none !important;
    }

    .mobile{
      display: block !important;
    }
    .info {
      width: 305px;
      height: max-content;
      display: flex;
      flex-wrap: wrap;
      line-height: 120%;
      padding: 0 24px;
      justify-content: center;
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
      width: 100%;
      font-size: 16px;
      color: #424242;
      line-height: 130%;
      text-align: center;
      padding: 0 4px;
    }

  }

  @media (min-width: 627px){
    *{
      width: 831px;

    }

    article{
      background: transparent;
      height: 361px;
      border-radius: 6px;
      border: transparent 0 solid;
      width: max-content;
      padding: 32px 0 0 24px;

    }

    .mobile{
      display: none;
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
      top: 10px;
      right: 20px;
    }

    header{
      font-size: 36px;
      font-weight: 800;
      z-index: 4;
      color: #424242;
      margin-bottom: 15px;
      width: max-content;
      height: max-content;
      line-height: 120%;
    }
    .info {
      width: 305px;
      height: max-content;
      display: flex;
      flex-wrap: wrap;
      margin-bottom: 13px;
      line-height: 120%;
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
      line-height: 130%;
    }


    .bg-custom-cont{
      position: absolute;
      top: 0;
      z-index: -1;
    }

    .bg-custom{
      position: relative;
      display: flex;
      > .white{
        width: 320px;
        height: 361px;
        background: #fff;
        border: transparent 0;
        border-radius: 6px 0 0 6px;

      }
      > .gradient{
        width: 310px;
        height: 361px;
        background: rgb(255,255,255);
        background: linear-gradient(90deg, rgba(255,255,255,1) 0%, rgba(255,255,255,0) 100%);
        z-index: 1;
        //position: absolute;
        top: 0;
      }
      > img{
        width: 510px;
        height: 361px;
        position: absolute;
        right: 0px;
      }

    }
  }

</style>
