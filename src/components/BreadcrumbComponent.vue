<template>
  <nav style="--bs-breadcrumb-divider: '→';" aria-label="breadcrumb">
    <ol class="breadcrumb">
      <li class="breadcrumb-item ">Главная</li>
      <li class="breadcrumb-item active" aria-current="page">Каталог</li>
    </ol>
  </nav>
</template>

<script>
export default {
  name: "BreadcrumbComponent"
}
</script>

<style scoped>
  nav{
    padding-bottom: 32px;
  }
</style>
