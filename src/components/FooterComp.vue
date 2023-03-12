<template>
  <div class="container">
    <div class="d-flex justify-content-center mb-4">
      <div class="socialmedia">
        <a href="https://www.linkedin.com/company/coderamx" target="_blank">
          <i class="bi bi-linkedin social-icon"></i>
        </a>
        <a href="https://www.facebook.com/codera.mx" target="_blank">
          <i class="bi bi-facebook social-icon"></i>
        </a>
        <a href="https://wa.link/a1sknx" target="_blank">
          <i class="bi bi-whatsapp social-icon"></i>
        </a>
        <a href="mailto:coderabcs@gmail.com">
          <i class="bi bi-envelope social-icon"></i>
        </a>
      </div>
    </div>
    <div class="row">
      <p class="ts-small text-center">codera 2023 - Todos los derechos reservados</p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.container {
  padding: 3rem 2rem;
  justify-content: center;
  .socialmedia {
    display: flex;
    flex-direction: row;
    column-gap: 2.5rem;
    a {
      display: flex;
      background-color: transparent;
      transition: 0.3s ease-in-out;
      text-decoration: none;
      justify-content: center;
      align-items: center;
      border-radius: 50%;
      width: 48px;
      height: 48px;
      color: inherit;
      &:hover {
        background-color: #ebebeb;
      }
      .social-icon {
        font-size: 28px;
      }
    }
  }
}
</style>