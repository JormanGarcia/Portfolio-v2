<template>
  <div>
    <Header />
    <Nuxt />
  </div>
</template>

<style>

@import url('https://fonts.googleapis.com/css2?family=Inconsolata:wght@300;400;500;600;700;800;900&display=swap');

:root {
  --main-color: #2C3840;
  --background-color: #fafafa;
  --highlight-color: #50F2C4;
  --highlight-color-dark: #17BFA0;
  --transition-nav: .3s ease;
  --menu-size: 55px;
}

* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-family: 'Inconsolata', monospace;
}

a {
  color: black;
  text-decoration: none;

}

body {
  background: var(--background-color);
  overflow-x: hidden;
}

.container {
  width: 90%;
  margin: auto;
  max-width: 1100px;
  margin-top: 50px;
}

</style>
