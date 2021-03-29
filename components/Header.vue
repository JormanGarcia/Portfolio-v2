<template>
    <header>
        <transition name="menu" appear>

            <div class="menu-container"  :class="{active: isNavOpen}" @click="isNavOpen = !isNavOpen" >
                <div class="menu" :class="{active: isNavOpen}" >
                    <div class="line top"></div>
                    <div class="line center"></div>
                    <div class="line bottom"></div>
                </div>
            </div>

        </transition>


        <Nav :isNavOpen="isNavOpen" />
    </header>
</template>

<script>
export default {
    data: function() {
        return {
            isNavOpen: false
        }
    }
}
</script>

<style>
    header {
        display: flex;
        justify-content: flex-end;
        padding: 25px 15px;
    }

    .menu-container {
        -webkit-tap-highlight-color: transparent;
    }

    .menu {
        width: var(--menu-size);
        height: var(--menu-size);
        border-radius: 50%;
        background: var(--main-color);
        overflow: hidden;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        cursor: pointer;
        transition: var(--transition-nav);
        position: absolute;
        top: 10px;
        right: 10px;
        z-index: 1000;
    }




    .line {
        width: 25px;
        height: 3px;
        background: var(--background-color);
        margin-bottom: 5px;
        transition: var(--transition-nav);
    }

    .line.top {
        width: 15px;
    }
    .line.bottom {
        width: 15px;
    }

    .menu.active {
        background: var(--background-color);
        transform: rotate(-270deg) scale(.9);
    }

    .menu.active .line {
        background: var(--main-color);
    }

    .menu div:last-of-type {
        margin: 0;
    }


    .menu-enter {
        opacity: 0;
        transform: translateX(-100px)
    }

    .menu-enter-active {
        transition: .3s;
    }
</style>
