<template>
  <BreadcrumbComponent/>
  <CardComponent/>
</template>

<script>
import BreadcrumbComponent from "@/components/BreadcrumbComponent";
import CardComponent from "@/components/CardComponent";

export default {
  name: "ContentComponent",
  components: {
    BreadcrumbComponent, CardComponent
  }

}
</script>

<style scoped>

</style>
