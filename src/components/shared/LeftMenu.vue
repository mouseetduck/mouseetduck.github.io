<script setup>
import { RouterLink } from 'vue-router'
import ImgFcyzUrl from '../images/Icon-fcyz.png'
import { ref } from 'vue';

const menu = ref([
  {
    router:"/",
    name:"主页"
  },
  {
    router:"/figures",
    name:"人物"
  },
  {
    router:"/history",
    name:"校史"
  },
  {
    router:"/reposity",
    name:"资料库"
  },
  {
    router:"/others",
    name:"其它"
  },
  {
    router:"/about",
    name:"关于"
  }
])

</script>

<template>

    <left-menu-button><img :src="ImgFcyzUrl" alt="图片击败" /></left-menu-button>

    <ul>
      <li class ="logo">
        <img :src="ImgFcyzUrl" alt="图片击败！！" />
        <h4>肥城市第一高级中学</h4>
      </li>

      <template v-for="item in menu">
        <RouterLink :to="item.router">
          <li> {{ item.name }} </li>
        </RouterLink>
      </template>
     
    </ul>
</template>


<style scoped>
left-menu-button {
  /*
  display: none;
  */

  position: fixed;
  top: 3rem;
  left: 0rem;

  background-color: var(--color-background-soft);
  opacity: 0;

  border-radius: 0.4rem;

  width: 2.5rem;
  height: 2.5rem;

}

left-menu-button img{
  width: 75%;
  height:75%;

  margin: auto;

  opacity: 0.8;

  animation:image-rotate 5s;
  animation-timing-function:linear;
  animation-iteration-count:infinite;
}

ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
 }

ul li {
  margin: 0;
  padding: var(--menu-height) 0 var(--menu-height) 0 ;
  border-bottom: 1px solid var(--color-border);

  text-align: center;
}

ul li.logo {
  padding: var(--menu-height) 0 var(--menu-height) 0;
}

ul a.router-link-exact-active {
  color: var(--color-text);
}

ul a.router-link-exact-active:hover {
  background-color: transparent;
} 

ul li.logo img{
  width: 75%;
  height:75%;

  animation:image-rotate 5s;
  animation-timing-function:linear;
  animation-iteration-count:infinite;
}

ul li.logo h4{
  margin: 0 0.8rem 0 0.8rem;

  font-weight: 750;
  font-size: 0.9rem;
}



@keyframes image-rotate {
    from {transform: rotate(0deg);} 
    to {transform: rotate(360deg);} 
}

/*
@media (max-width: 768px) {
  ul li:not(.logo) {
    float: left;
  }
}
*/

@media (hover: hover) {
  ul li:not(.logo):hover {
    background-color: hsla(160, 100%, 37%, 0.2);
  }
}

@media (max-width: 768px) {
  ul {
    display: none;
  }

  left-menu-button {
    display: flex;
    opacity: 0.8;

    left: 2rem;

    transition: 0.4s;
  }
}
</style>