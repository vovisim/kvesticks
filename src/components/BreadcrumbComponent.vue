<template>
  <nav style="--bs-breadcrumb-divider: '→';" aria-label="breadcrumb" >
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
    height: max-content;
    padding: 24px 162px 32px 162px;
  }
  ol{
    margin: 0;
  }

  @media (max-width: 627px) {
    * {
      display: none;
    }

  }
</style>
