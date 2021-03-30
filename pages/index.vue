<template>
  <div class="container hero">
    <div class="helloWorld">
      Jorman Garcia
    </div>

    <p>Desarrollador Web <span>Front End</span></p>

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
    margin-bottom: 10px;
  }

  .helloWorld span {
    color: var(--highlight-color-dark)
  }

  .hero {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    overflow: hidden;
  }
  .hero p{
    margin-bottom: 30px;
  }
  .hero a {
    border: 3px solid var(--main-color);
    border-radius: 50%;
    width: 100px;
    height: 100px;
    display: flex;
    justify-content: center;
    align-items: center;
    font-weight: 900;
    animation: rotate 10s infinite linear;
    font-size: 12px;
    transition: .2s ease;
  }

  .hero a:hover {
    background: var(--main-color);
    color: var(--highlight-color);

  }

  @keyframes rotate {
    from {transform: rotate(0);}
    to {transform: rotate(360deg);}
  }
</style>
