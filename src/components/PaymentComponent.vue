<template>
  <div class="PaymentC">
    <div class="MainItem">
      <div class="">Принимаем к оплате</div>
      <div class="">
        <div class="">
          <img src="@/assets/PaymentComponent/sber.svg" alt="">
          <img src="@/assets/PaymentComponent/mastercard.svg" alt="">
          <img src="@/assets/PaymentComponent/visa.svg" alt="">
          <img src="@/assets/PaymentComponent/mir.svg" alt="">
        </div>
      </div>
    </div>

    <div class="2">Я из другой страны —</div>
    <div class="2">как оплатить?</div>

    <button class="MainItem">
      <span class="">Купить квест</span>
      <span class="">{{price}}₽</span>
    </button>
  </div>
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
  .PaymentC{
    width: 261px;
    padding: 20px;
    display: flex;
    flex-direction: column;
    align-items: center;
    background: #fff;
  }
</style>
