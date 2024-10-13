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
