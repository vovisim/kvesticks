<template>
  <div class="app">
    <NavBar/>
    <main>
      <ContentComponent/>
      <PaymentComponent/>
    </main>
  </div>
</template>

<script>
import NavBar from "@/components/NavBar";
import ContentComponent from "@/components/ContentComponent";
import PaymentComponent from "@/components/PaymentComponent";

export default {
  name: 'App',
  components: {
    NavBar, ContentComponent, PaymentComponent
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


}
</style>
