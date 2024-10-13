<template>
  <Carousel :items-to-show="1.25" :wrap-around="false">
    <Slide v-for="index in revuesData" :key="index">
      <revue_component :revueData="index"/>
    </Slide>

    <template #addons>
      <Pagination />
    </template>
  </Carousel>
</template>

<script>
import { defineComponent } from 'vue'
import { Carousel, Slide, Pagination } from 'vue3-carousel'
import 'vue3-carousel/dist/carousel.css'
import revue_component from "@/components/revue_component";
export default defineComponent({
  name: 'ExamplePagination',

  components: {
    Pagination,
    Carousel,
    Slide,
    revue_component
  },
  props: {
    revuesData: {}
  },
  data: () => ({
    // carousel settings
    settings: {
      itemsToShow: 1,
      snapAlign: 'start',
    },

  }),
})
</script>


<style>
  .carousel {
    text-align: start;

  }
  .carousel__item {
    width: max-content;
    display: flex;
    justify-content: start;
    align-items: start;
  }

</style>
