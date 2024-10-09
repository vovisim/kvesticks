<template>
  <div class="app">
    <NavBar/>
    <BreadcrumbComponent/>
    <main>
      <CardComponent/>
      <PaymentComponent v-if="false"/>
    </main>
  </div>
</template>

<script>
import NavBar from "@/components/NavBar";
import BreadcrumbComponent from "@/components/BreadcrumbComponent";
import CardComponent from "@/components/CardComponent";
import PaymentComponent from "@/components/PaymentComponent";

export default {
  name: 'App',
  components: {
    NavBar, BreadcrumbComponent, CardComponent, PaymentComponent
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Open Sans', sans-serif;

}

main {
  padding: 0 162px;
  width: 100%;
  padding-top: 24px !important;
  display: flex;

}
</style>
