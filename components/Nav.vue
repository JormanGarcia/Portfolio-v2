<template>
<transition name="nav">

    <nav  v-if="isNavOpen" >
        <div>Hola</div>
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
    color: var(--highlight-color);

    position: absolute;
    top: 0px;
    right: 0px;
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;

}

.nav-enter-active,
.nav-leave-active {
  transition: var(--transition-nav);

}

.nav-enter,
.nav-leave-to {
  transform: translateY(-100%);
}
</style>
