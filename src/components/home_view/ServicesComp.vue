<template>
  <div class="services-comp">
    <div class="container">
      <div class="row">
        <div class="col col-12 col-md-4">
          <div class="card-section">
            <div class="circle-img">
              <img src="@/assets/img/ecommerce-website.png" alt="ecommerce" />
            </div>
            <h3 class="ts-h2 ff-belfast">Sitios web</h3>
            <p class="ts-h3">
              Desarrollamos tu sitio web para que puedas mostrar tu negocio, productos o servicios.
            </p>
          </div>
        </div>

        <div class="col col-12 col-md-4">
          <div class="card-section">
            <div class="circle-img">
              <img src="@/assets/img/social-media-post.png" alt="landingpage" />
            </div>
            <h3 class="ts-h2 ff-belfast">Landing Page</h3>
            <p class="ts-h3">
              Consigue que tus clientes se enganchen a tu negocio con una landing page.
            </p>
          </div>
        </div>

        <div class="col col-12 col-md-4">
          <div class="card-section">
            <div class="circle-img">
              <img src="@/assets/img/business-analysis.png" alt="business" />
            </div>
            <h3 class="ts-h2 ff-belfast">Sistemas web</h3>
            <p class="ts-h3">
              Construimos sistemas a la medida para que puedas automatizar tus procesos de negocio.
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ServicesComp",
};
</script>

<style lang="scss" scoped>
.services-comp {
  width: 100%;
  height: fit-content;
  margin-bottom: 100px;

  .card-section {
    width: 100%;
    height: fit-content;
    padding: 20px;
    border-radius: 18px;
    background-color: #fff;
    transition: var(--transition-normal);
    margin-bottom: 60px;

    .circle-img {
      width: 100px;
      height: 100px;
      border-radius: 50%;
      background-color: #e4e4e4;
      margin: 0 auto;
      margin-top: -50px;
      display: flex;
      justify-content: center;
      align-items: center;

      img {
        width: 300px;
        transform: scale(1.3);
        transition: var(--transition-normal);
      }
    }

    h3 {
      text-align: center;
      margin-top: 20px;
    }

    p {
      text-align: center;
      margin-top: 20px;
    }
  }

  .card-section:hover {
    box-shadow: 0 0 20px 10px rgba(0, 0, 0, 0.05);

    .circle-img {
      img {
        transform: scale(1.5);
      }
    }
  }
}
</style>
