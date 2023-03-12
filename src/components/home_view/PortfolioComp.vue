<template>
  <div class="portfolio-comp">
    <div class="container">
      <div class="row mb-5">
        <h1 class="ts-bigger ff-belfast">Nuestro trabajo</h1>
        <p class="ts-h2">Conoce un poco de lo que hemos realizado</p>
      </div>

      <!-- LANDFINDER MEXICO -->
      <div class="row mb-5">
        <div class="col col-12 col-md-6 col-lg-4 mb-5 mb-sm-0 order-1 order-sm-0">
          <div class="portfolio-img portfolio-img-1">
            <a href="https://landfindermexico.com" target="_blank">
              <i class="bi bi-box-arrow-up-right"></i>
            </a>
          </div>
        </div>

        <div class="col col-12 col-md-6 col-lg-8 mb-5 mb-sm-0">
          <div class="portfolio-info">
            <p class="ts-h1 tc-title tw-regular mb-2">Land Finder México</p>
            <p class="ts-biggest tc-title lh-normal mb-3">
              Plataforma para la compra y venta de terrenos en aportación
            </p>
            <p class="ts-h2 tc-text-light">web, development, real estate</p>
          </div>
        </div>
      </div>

      <!-- TRESAMCAPITAL -->
      <div class="row mb-5">
        <div class="col col-12 col-md-6 col-lg-8 col-lg-4 mb-5 mb-sm-0">
          <div class="portfolio-info">
            <p class="ts-h1 tc-title tw-regular mb-2">Tresam Capital</p>
            <p class="ts-biggest tc-title lh-normal mb-3">
              Firma de inversión dedicada a la alta gama de activos en distintos
              sectores
            </p>
            <p class="ts-h2 tc-text-light">web, development, investment</p>
          </div>
        </div>

        <div class="col col-12 col-md-6 col-lg-4 mb-5 mb-sm-0">
          <div class="portfolio-img portfolio-img-2">
            <a href="https://tresamcapital.com" target="_blank">
              <i class="bi bi-box-arrow-up-right"></i>
            </a>
          </div>
        </div>
      </div>

      <!-- FORM TYPER -->
      <div class="row mb-5">
        <div class="col col-12 col-md-6 col-lg-4 mb-5 mb-sm-0 order-1 order-sm-0">
          <div class="portfolio-img portfolio-img-3">
            <a href="https://formtyper.vercel.app/" target="_blank">
              <i class="bi bi-box-arrow-up-right"></i>
            </a>
          </div>
        </div>
        <div class="col col-12 col-md-6 col-lg-8 mb-5 mb-sm-0">
          <div class="portfolio-info">
            <p class="ts-h1 tc-title tw-regular mb-2">Form typer</p>
            <p class="ts-biggest tc-title lh-normal mb-3">
              Sistema de registro de datos de afiliados para asociaciones
            </p>
            <p class="ts-h2 tc-text-light">web, design, development</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.portfolio-comp {
  width: 100%;

  .portfolio-img {
    height: 70vh;
    background-size: cover;
    background-position: center;
    position: relative;
    border-radius: 18px;

    a {
      position: absolute;
      top: 50%;
      left: 50%;
      background-color: #0000006b;
      width: 80px;
      height: 80px;
      border-radius: 50%;
      transform: translate(-50%, -50%);
      color: var(--color-white);
      font-size: 2rem;
      transition: all 0.3s ease-in-out;
      display: grid;
      place-items: center;
      opacity: 0;

      i {
        color: white;
      }
    }

    &:hover {
      a {
        opacity: 1;
      }
    }
  }

  .portfolio-img-1 {
    background-image: url("~@/assets/img/portfolio-1.jpg");
  }

  .portfolio-img-2 {
    background-image: url("~@/assets/img/portfolio-2.jpg");
  }

  .portfolio-img-3 {
    background-image: url("~@/assets/img/portfolio-3.jpg");
  }

  .portfolio-info {
    display: flex;
    flex-direction: column;
    justify-content: center;
    height: 100%;
    padding: 0 4rem;
  }
}

@media only screen and (max-width: 992px) {
  .portfolio-comp {

    .portfolio-img {
      a {
        opacity: 1;
      }
    }
    .portfolio-info {
      padding: 0 1rem;

      .ts-h1 {
        font-size: 1.5rem;
      }
      .ts-biggest {
        font-size: 2.5rem;
      }
    }
  }
}
</style>
