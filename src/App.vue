<template>
  <div class="app">
    <NavBar/>
    <BreadcrumbComponent/>
    <main>
      <div class="Top">
        <CardComponent/>
        <PaymentComponent />
      </div>
      <RevueComponent/>
      <div class="buyKvest mobile">
        <button class="buyKvestItem">
          <span class="">Купить квест</span>
          <span class="">{{price}}₽</span>
        </button>
      </div>
    </main>
  </div>
</template>

<script>
import NavBar from "@/components/NavBar";
import BreadcrumbComponent from "@/components/BreadcrumbComponent";
import CardComponent from "@/components/CardComponent";
import PaymentComponent from "@/components/PaymentComponent";
import RevueComponent from "@/components/RevueComponent";

export default {
  name: 'App',
  components: {
    NavBar, BreadcrumbComponent, CardComponent, PaymentComponent, RevueComponent
  },
  data(){
    return{
      price: 500
    }
  }
}
</script>

<style>
.app{
  width: 100%;

}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Open Sans', sans-serif;
  /*border: 1px red solid;*/
  line-height: 130%;
}

main {
  padding: 0 162px;
  width: 100%;
  display: flex;
  flex-direction: column;
}

.Top{
  justify-content: space-between;
  display: flex;
  margin-bottom: 48px;

}

@media (max-width: 627px) {

  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Open Sans', sans-serif;
    /*border: 1px red solid;*/
    line-height: 130%;
  }
  main{
    padding: 0;
  }



}
</style>

<style scoped>
  @media (min-width: 627px) {
    .mobile {
      display: none !important;
    }
  }


  .buyKvest {
    width: 100%;
    height: 72px;
    display: flex;
    justify-content: center;
    padding: 10px 12px;
    background: #FFFFFF;
    border-radius: 7px 7px 0 0;
    box-shadow: 0 -2px 3px 0 rgba(0, 0, 0, 0.15);
    position: fixed;
    bottom: 0;
  }
  .buyKvestItem{
    display: flex;
    justify-content: space-between;
    background: #F77833;
    color: #FFFFFF;
    font-size: 16px;
    font-weight: 600;
    line-height: 20px;
    border: 0px transparent;
    letter-spacing: -1%;
    padding: 7px 23px;
    height: 52px;
    align-items: center;
    border-radius: 7px;
    width: 100%;
  }
</style>
