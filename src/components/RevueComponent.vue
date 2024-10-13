<template>
  <div class="RevueComponent">
    <header>
      <div class="head">Отзывы клиентов</div>
      <div class="count">{{count}}</div>
    </header>
    <ul class="desctop">
      <li v-for="index in revuesData" :key="index">
        <revue_component :revueData="index"/>
      </li>
    </ul>
    <div class="slider-container mobile">
      <div class="borderBox">
        <div class="item" v-for="index in revuesData" :key="index">
          <revue_component :revueData="index"/>
        </div>
      </div>
    </div>

    <div class="buton">
      <button>Смотреть все отзывы</button>
    </div>



  </div>
</template>

<script>

import revue_component from "@/components/revue_component";
export default {
  name: "RevueComponent",
  components: {
    revue_component
  },
  data(){
    return{
      count: 182,
      revuesData: {
        0: {
          date: "14 февраля 2024",
          aboutPlayers: "Константин (12 игроков 36-50 лет) ",
          stars: 5,
          header: "День святого Валентина",
          description: "Понравилось, что вопросы хоть и объединены одной темой, были не похожи друг на друга. Разные страны и эпохи — есть где разгуляться фантазии. И если сначала мы пытались искать правильные ответы, то по ходу игры стало интереснее и смешнее запутать других игроков."
        },
        1:{
          date: "14 февраля 2024",
          aboutPlayers: "Светлана (2 игрока 36 лет)",
          stars: 5,
          header: "День Рождения",
          description: "Понравилось, что вопросы хоть и объединены одной темой, были не похожи друг на друга. Разные страны и эпохи — есть где разгуляться фантазии. И если сначала мы пытались искать правильные ответы, то по ходу игры стало интереснее и смешнее запутать других игроков."
        },
        2:{
          date: "14 февраля 2024",
          aboutPlayers: "Светлана (2 игрока 36 лет)",
          stars: 5,
          header: "День Рождения",
          description: "Понравилось, что вопросы хоть и объединены одной темой, были не похожи друг на друга. Разные страны и эпохи — есть где разгуляться фантазии. И если сначала мы пытались искать правильные ответы, то по ходу игры стало интереснее и смешнее запутать других игроков."
        },
        3:{
          date: "14 февраля 2024",
          aboutPlayers: "Светлана (2 игрока 36 лет)",
          stars: 5,
          header: "День Рождения",
          description: "Понравилось, что вопросы хоть и объединены одной темой, были не похожи друг на друга. Разные страны и эпохи — есть где разгуляться фантазии. И если сначала мы пытались искать правильные ответы, то по ходу игры стало интереснее и смешнее запутать других игроков."
        },
        4:{
          date: "14 февраля 2024",
          aboutPlayers: "Светлана (2 игрока 36 лет)",
          stars: 5,
          header: "День Рождения",
          description: "Понравилось, что вопросы хоть и объединены одной темой, были не похожи друг на друга. Разные страны и эпохи — есть где разгуляться фантазии. И если сначала мы пытались искать правильные ответы, то по ходу игры стало интереснее и смешнее запутать других игроков."
        },
        5: {
          date: "14 февраля 2024",
          aboutPlayers: "Константин (12 игроков 36-50 лет) ",
          stars: 5,
          header: "День святого Валентина",
          description: "Понравилось, что вопросы хоть и объединены одной темой, были не похожи друг на друга. Разные страны и эпохи — есть где разгуляться фантазии. И если сначала мы пытались искать правильные ответы, то по ходу игры стало интереснее и смешнее запутать других игроков."
        },
        6:{
          date: "14 февраля 2024",
          aboutPlayers: "Светлана (2 игрока 36 лет)",
          stars: 5,
          header: "День Рождения",
          description: "Понравилось, что вопросы хоть и объединены одной темой, были не похожи друг на друга. Разные страны и эпохи — есть где разгуляться фантазии. И если сначала мы пытались искать правильные ответы, то по ходу игры стало интереснее и смешнее запутать других игроков."
        },
        7:{
          date: "14 февраля 2024",
          aboutPlayers: "Светлана (2 игрока 36 лет)",
          stars: 5,
          header: "День Рождения",
          description: "Понравилось, что вопросы хоть и объединены одной темой, были не похожи друг на друга. Разные страны и эпохи — есть где разгуляться фантазии. И если сначала мы пытались искать правильные ответы, то по ходу игры стало интереснее и смешнее запутать других игроков."
        },
        8:{
          date: "14 февраля 2024",
          aboutPlayers: "Светлана (2 игрока 36 лет)",
          stars: 5,
          header: "День Рождения",
          description: "Понравилось, что вопросы хоть и объединены одной темой, были не похожи друг на друга. Разные страны и эпохи — есть где разгуляться фантазии. И если сначала мы пытались искать правильные ответы, то по ходу игры стало интереснее и смешнее запутать других игроков."
        },
        9:{
          date: "14 февраля 2024",
          aboutPlayers: "Светлана (2 игрока 36 лет)",
          stars: 5,
          header: "День Рождения",
          description: "Понравилось, что вопросы хоть и объединены одной темой, были не похожи друг на друга. Разные страны и эпохи — есть где разгуляться фантазии. И если сначала мы пытались искать правильные ответы, то по ходу игры стало интереснее и смешнее запутать других игроков."
        }

      }
    }
  },

}

</script>

<style scoped lang="scss">


  //@media(min-width: 1200px){
  //  .slide {
  //    padding: 3rem;
  //  }
  //}
  //
  //.slide img{
  //  max-width: 100%;
  //  max-height: 100%;
  //  transition: transform 0.3s ease-in-out;
  //  box-shadow: 5px 5px 50px -1px var(--shadow);
  //  border-radius: 4px;
  //  user-select: none;
  //}
  //
  //.grabbing {
  //  cursor: grabbing;
  //}
  //
  //.grabbing .slide img{
  //  transform: scale(0.9);
  //  box-shadow: 5px 5px 40px -1px var(--shadow);
  //}

  @media (max-width: 627px) {
    * {
      box-sizing: border-box;
      padding: 0;
      margin: 0;
    }
    .slider-container {
      padding: 0 12px;
    }
    .borderBox {
      display: flex !important;
      flex-direction: row !important;
      flex-wrap: nowrap;
      overflow-x: auto;
      width: 350px;
      box-sizing: border-box;
      gap: 10px;
    }

    .borderBox::-webkit-scrollbar {
      width: 10px;
      height: 10px;
    }

    .borderBox::-webkit-scrollbar-thumb {
      background-color: #d32121;
      border-radius: 10px;
    }

    .borderBox::-webkit-scrollbar{
      background-color: #0a0a73;
      border-radius: 10px;
    }

    button{
      width: 334px;
      height: 52px;
      background: #F77833;
      color: #FFFFFF;
      font-size: 16px;
      font-weight: 700;
      line-height: 20px;
      letter-spacing: -1%;
      border: transparent 0 solid;
      border-radius: 8px;
      margin: 0 13px;
    }


    .desctop{
      display: none !important;
    }
    .mobile{
      display: block;
    }
    .head{
      font-size: 24px;
      font-weight: 800;
      line-height: 120%;
    }
    header{
      display: flex;
      margin-bottom: 24px;
      width: 100%;
      padding: 0 30px;
      > .head {
        margin-right: 10px;
      }
      > *{
        width: max-content;
      }
    }

  }
  @media (min-width: 627px) {
    .desctop{
      display: flex;
    }
    .mobile{
      display: none !important;
    }

    .RevueComponent {
      width: 831px;
      display: flex;
      flex-direction: column;

    }

    ul {
      display: flex;
      justify-content: space-around;
      overflow-x: auto;

      &::-webkit-scrollbar{
        background-color: #DDDDDD;
        border-radius: 7px;
        height: 15px;

      }
      &::-webkit-scrollbar-thumb {
        background: #A8A8A8;
        width: 260px;
        border-radius: 7px;
      }

    }
    li{
      margin-right: 24px;
      &:last-child{
        margin-right: 0;
      }

      margin-bottom: 16px;
    }
    .head{
      font-size: 28px;
      font-weight: 800;
      line-height: 120%;
    }
    header{
      display: flex;
      margin-bottom: 24px;
      > .head {
        margin-right: 10px;
      }
      > *{
        width: max-content;
      }
    }
    button{
      width: 437px;
      height: 52px;
      background: #F77833;
      color: #FFFFFF;
      font-size: 16px;
      font-weight: 700;
      line-height: 20px;
      letter-spacing: -1%;
      border: transparent 0 solid;
      border-radius: 8px;
      margin-top: 24px;
    }

    .buton{
      display: flex;
      justify-content: center;
    }

  }




</style>
