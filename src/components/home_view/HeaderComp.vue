<template>
  <div class="header-comp">
    <div class="container">
      <div class="row align-items-center">
        <div class="col col-12 col-sm-7">
          <h1 class="main-title mb-4">
            El <span class="tc-primary">sitio web</span> que tu negocio
            necesita
          </h1>
          <p class="ts-h2 w-75 mb-4">
            En <b>codera</b> te ofrecemos el expertise y el equipo para desarrollar
            el sitio web para tu negocio.
          </p>

          <a href="#contact" class="fill">Cotiza tu idea</a>
        </div>

        <div class="col col-12 col-sm-5 d-none d-sm-flex">
          <lottie-player src="./lottie-person.json" background="transparent"  speed="1"  style="width: 100%;" loop autoplay></lottie-player>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HomeView",
};
</script>

<style lang="scss" scoped>
.header-comp {
  height: fit-content;
  min-height: 80vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.main-title {
  font-size: 3.6rem;
  font-family: var(--belfast-font);
}

.button-start-project {
  box-sizing: border-box;
  background-color: var(--color-secondary);
  padding: 0.6rem 1rem;
  text-decoration: none;
  color: var(--color-text);
}

.fill {
  font-size: 20px;
  letter-spacing: 1px;
  padding: 13px 50px 13px;
  outline: 0;
  border: 1px solid rgb(26, 26, 26);
  cursor: pointer;
  position: relative;
  text-decoration: none;
  color: var(--color-title);
  font-weight: var(--font-medium);
  font-family: var(--belfast-font);
  background-color: rgba(0, 0, 0, 0);
}

.fill::after {
  content: "";
  background-color: var(--color-secondary);
  width: 100%;
  z-index: -1;
  position: absolute;
  height: 100%;
  top: 7px;
  left: 7px;
  transition: 0.2s;
}

.fill:hover::after {
  top: 0px;
  left: 0px;
}
</style>