<template>
<transition name="nav">

    <nav  v-if="isNavOpen" >
        <nuxt-link to="/">Inicio</nuxt-link>
        <nuxt-link to="/">Sobre Mí</nuxt-link>
        <nuxt-link to="/">Portafolio</nuxt-link>


        <p class="email">Jormanj_@outlook.com</p>
    </nav>

</transition>
</template>

<script>
export default {
    props: ["isNavOpen"]
}
</script>

<style>
nav {
    background: var(--main-color);

    position: absolute;
    top: 0px;
    right: 0px;
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-end;
    padding-right: 20px;

}

nav a{
    color: var(--highlight-color);
    font-size: 35px;
    font-weight: 900;
    margin-bottom: 10px;
    transition: .1s;
}

nav a:hover {
    color: var(--background-color);
    text-shadow: 1px 1px 0 var(--highlight-color-dark);
}



.nav-enter-active,
.nav-leave-active {
  transition: var(--transition-nav);

}

.nav-enter,
.nav-leave-to {
  transform: translateY(-100%);
}

.email {
    color: var(--background-color);
    font-weight: 700;
    position: absolute;
    bottom: 20px;
    right: 20px;
    font-size: 14px;
}
</style>
