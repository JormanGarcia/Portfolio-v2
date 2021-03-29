<template>
  <div class="container hero">
    <div class="helloWorld">
      Jorman Garcia
    </div>

    <p>Desarrollador Web orientado al <span>Front End</span></p>

    <nuxt-link to="/portafolio">Portafolio</nuxt-link>
  </div>
</template>

<script>
export default {
  
}
</script>

<style>
  .helloWorld {
    font-size: 35px;
    font-weight: 900;
  }

  .helloWorld span {
    color: var(--highlight-color-dark)
  }

  .hero {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  .hero a {
    border: 3px solid var(--main-color);
    border-radius: 50%;
    width: 120px;
    height: 120px;
    display: flex;
    justify-content: center;
    align-items: center;
    font-weight: 900;
    transition: .2s ease;
    position: absolute;
    bottom: 20px;
    right: 20px;
    transform: rotate(-20deg)
  }

  .hero a:hover {
    width: 110px;
    height: 110px;
    transform: rotate(0deg) scale(.9);
    background: var(--main-color);
    color: var(--highlight-color);
  }
</style>
