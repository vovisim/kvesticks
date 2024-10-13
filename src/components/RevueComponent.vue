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
    <div class="slider-container-out mobile">
      <div class="slider-container" ref="slider">
        <div class="slide" v-for="index in revuesData" :key="index">
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
  mounted() {
    window.addEventListener('resize', this.setPositionByIndex);
    window.oncontextmenu = (event) => {
      event.preventDefault();
      event.stopPropagation();
      return false;
    };
  },
  beforeUnmount() {
    window.removeEventListener('resize', this.setPositionByIndex);
  },
  methods: {
    pointerDown(index) {
      return (event) => {
        this.currentIndex = index;
        this.startPos = event.clientX;
        this.isDragging = true;
        this.animationID = requestAnimationFrame(this.animation);
        this.$refs.slider.classList.add('grabbing');
      };
    },
    pointerMove(event) {
      if (this.isDragging) {
        const currentPosition = event.clientX;
        this.currentTranslate = this.prevTranslate + currentPosition - this.startPos;
      }
    },
    pointerUp() {
      cancelAnimationFrame(this.animationID);
      this.isDragging = false;
      const movedBy = this.currentTranslate - this.prevTranslate;

      // Snap to the next or previous slide
      if (movedBy < -100 && this.currentIndex < this.slides.length - 1) {
        this.currentIndex += 1;
      }
      if (movedBy > 100 && this.currentIndex > 0) {
        this.currentIndex -= 1;
      }

      this.setPositionByIndex();
      this.$refs.slider.classList.remove('grabbing');
    },
    animation() {
      this.setSliderPosition();
      if (this.isDragging) {
        this.animationID = requestAnimationFrame(this.animation);
      }
    },
    setPositionByIndex() {
      this.currentTranslate = this.currentIndex * -window.innerWidth;
      this.prevTranslate = this.currentTranslate;
      this.setSliderPosition();
    },
    setSliderPosition() {
      this.$refs.slider.style.transform = `translateX(${this.currentTranslate}px)`;
    }
  },
  data(){
    return{
      count: 182,
      isDragging: false,
      startPos: 0,
      currentTranslate: 0,
      prevTranslate: 0,
      currentIndex: 0,
      animationID: null,
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
      height: max-content;
      width: 100%;
      display: inline-flex;
      overflow: hidden;
      scrollbar-width: none;
      transform: translateX(0);
      will-change: transform;
      transition: transform 0.3s ease-out;
      cursor: grab;
      gap: 10px;
    }
    .slider-container-out{
      padding: 12px;
    }
    .slide{
      display: flex;
      align-items: center;
      justify-content: center;
      width: 261px;
      height: 432px;
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
