<script setup>
import { RouterView } from 'vue-router'
import LeftMenu from './components/shared/LeftMenu.vue'
</script>

<template>
  <!--left-menu start-->
  <menu>
    <LeftMenu></LeftMenu>
  </menu>
  <!--left-menu end-->

  <!--content start-->
  <content>
    <RouterView />
  </content>
  <!--content end-->

</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

menu {
  display: block;
  position: fixed;
  left: 0;
  top: 0;

  padding: 0;
  margin: 0;

  height: 100%;
  width: var(--menu-gap);

  transition: 0.4s;
}

content {
  display: block;
  position: absolute;
  left: var(--menu-gap);
  top: 3rem;

  width: -webkit-fill-available;
  min-height: 35rem;

  border-style: solid;
  border-color: var(--color-border);
  border-top-left-radius: 1rem;
  border-bottom-left-radius: 1rem;

  background-color:var(--color-background);
  padding: 5rem 8rem 8rem 8rem;
  margin: 0;

  transition: 0.4s;
}

/*
.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}
*/

@media (max-width: 1024px) {
  menu {
    width: calc(var(--menu-gap) / 2);
  }

  content {
    left: calc(var(--menu-gap) / 2);
    padding: 2rem 3rem 3rem 3rem;
  }
  /*
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
  */
}
@media (max-width: 768px) {
  content {
    position: static;
    padding: 2rem 3rem 3rem 3rem;
    border-radius: 1rem;
  }
 
}
</style>

