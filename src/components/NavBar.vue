<template>
  <nav class="navbar navbar-expand-lg bg-body-tertiary justify-content-end">
    <div class="container-fluid">
      <button class="navbar-toggler border-0" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavDropdown" aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <a class="navbar-brand" href="#"><img src="@/assets/NavBar/logo.svg"></a>

      <a class="navbar-toggler border-0" aria-current="page" href="#">
        <img src="@/assets/NavBar/personal_account.svg" alt="">
      </a>


      <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <a class="nav-link" aria-current="page" href="#">
              <img src="@/assets/NavBar/contact.svg" alt="">
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">
              <img src="@/assets/NavBar/blog.svg" alt="">
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">
              <img src="@/assets/NavBar/personal_account.svg" alt="">
            </a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<script>

export default {
  name: "NavBar"
}
</script>

<style scoped>
  nav{
    box-shadow: 0 1px 4px rgba(0, 0, 0, 0.08);
    padding-top: 0;
    background: #FFFFFF;
  }
  .container-fluid {
    padding: 0 162px;

  }
  .nav-link{
    margin-left: 24px;
  }

  @media (max-width: 627px) {
    nav{
      width: 100%;
      padding: 0;
    }

    .container-fluid{
      padding: 0 0 !important;
    }

  }
</style>
