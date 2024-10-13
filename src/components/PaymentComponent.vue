<template>
  <aside class="PaymentC">
    <div class="MainItem">
      <div class="e1">Принимаем к оплате</div>
      <div class="bankIconsCont">
        <div class="bankIcons">
          <img src="@/assets/PaymentComponent/sber.svg" alt="">
          <img src="@/assets/PaymentComponent/mastercard.svg" alt="">
          <img src="@/assets/PaymentComponent/visa.svg" alt="">
          <img src="@/assets/PaymentComponent/mir.svg" alt="">
        </div>
      </div>
    </div>
    <div class="MainItem Country">
      <div class="">Я из другой страны —</div>
      <a href="https://kvestiks.ru/scenarios/o-boze-kakoj-muzcina#">как оплатить?</a>
    </div>


    <button class="MainItem">
      <span class="">Купить квест</span>
      <span class="">{{price}}₽</span>
    </button>
  </aside>
</template>

<script>
export default {
  name: "PaymentComponent",
  data(){
    return{
      price: 500
    }
  }
}
</script>

<style scoped lang="scss">

  @media (max-width: 627px) {
    .PaymentC {
      display: none !important;
    }

  }


  .PaymentC{
    width: 261px;
    padding: 20px;
    display: flex;
    flex-direction: column;
    align-items: center;
    background: #fff;
    height: max-content;
    border: 0 transparent;
    border-radius: 8px;
    box-shadow: 0 1px 4px rgba(0, 0, 0, 0.08);
  }

  .MainItem{
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    line-height: 120%;
  }

  .Country{
    display: flex;
    flex-direction: column;
    margin: 24px 0;
    align-items: center;
    font-size: 16px;
    > a {
      color: #F77833;
    }
    > div {
      color: rgba(56, 56, 56, 1);
    }
  }

  .bankIconsCont{
    width: 100%;
  }

  .bankIcons{
    display: flex;
    justify-content: space-around;
  }

  button{
    flex-direction: row !important;
    justify-content: space-around;
    padding: 16px 24px;
    background: #F77833;
    border: transparent 0;
    border-radius: 7px;
    color: #FFFFFF;
    font-size: 16px;
    font-weight: 600;
    line-height: 20px;
    letter-spacing: -1%;
  }

  .e1{
    font-size: 13px;
    color: rgba(56, 56, 56, 0.8);
    margin-bottom: 8px;
  }
</style>
