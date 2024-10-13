<template>
  <section>
    <div class="data">{{revueData.date}}</div>
    <div class="headRevue">
      <div class="aboutPlayers">{{revueData.aboutPlayers}}</div>
      <div class="stars">
        <ul v-for="i in revueData.stars" :key="i">
          <li><img src="@/assets/revue_component/Star.svg" alt=""></li>
        </ul>
      </div>
    </div>
    <div class="descriptionCont">
      <div class="descriptionContIns position-relative">
        <div class="Description">
          <div class="header">{{revueData.header}}</div>
          <div class="description">{{revueData.description}}</div>
        </div>

      </div>
    </div>


  </section>
</template>

<script>
export default {
  name: "revue_component",
  props: {
    revueData: {
      date: String,
      aboutPlayers: String,
      stars: Number,
      header: String,
      description: String
    }
  }
}
</script>

<style scoped lang="scss">

  section{
    background: #fff;
    padding: 30px 24px;
    display: flex;
    flex-direction: column;
    max-width: 261px;
    border: 0 solid transparent;
    border-radius: 8px;
    box-shadow: 0 1px 4px rgba(0, 0, 0, 0.08);
    max-height: 432px;
    width: 261px;
    > .data {
      color: #868686;
      font-size: 13px;
      margin-bottom: 16px;
    }


    .aboutPlayers {
      color: #383838;
      font-size: 14px;
    }

    .stars{
      display: flex;
      margin-bottom: 16px;

      > ul > li {
        margin-right: 8px;
      }
    }

    .header{
      color: #383838;
      font-size: 16px;
      line-height: 120%;
      margin-bottom: 12px;
      font-weight: 700;

    }
    .headRevue{
      height: 73px;
    }


  }
</style>
