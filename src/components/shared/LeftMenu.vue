<script setup>
import { RouterLink } from 'vue-router'
import ImgFcyzUrl from '../images/Icon-fcyz.png'
</script>
<template>
    <ul>
      <li class ="logo">
        <img :src="ImgFcyzUrl" alt="图片击败！！" />
        <h4>肥城市第一高级中学</h4>
      </li>
      <RouterLink to="/"><li>主页</li></RouterLink>
      <RouterLink to="/figures"><li>人物</li></RouterLink>
      <RouterLink to="/reposity"><li>资料库</li></RouterLink>
      <RouterLink to="/others"><li>其它</li></RouterLink>
      <RouterLink to="/about"><li>关于</li></RouterLink>
    </ul>
</template>


<style scoped>

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

@media (hover: hover) {
  ul li:not(.logo):hover {
    background-color: hsla(160, 100%, 37%, 0.2);
  }
}

</style>