<script setup>
const props = defineProps({
  url:String
});
</script>
<template>
  <div class="page-description">
    <img :src="url" alt="图片击败！！" />
    <div style="padding: 0 1rem 0 1rem;"><slot name="heading"></slot></div>
  </div>
  <br />
</template>
<style scoped>
div.page-description{
  background-color: var(--color-background-description);
  border:1px solid var(--color-border);

  border-left: 1rem solid var(--color-theme-1);

  font-size: small;
  text-align: center;

  margin: auto;
  width: 25%;
  height: 100px;

  display: flex;
  align-items: center;
  justify-content: space-around;

  overflow: hidden;
}
div.page-description img{
  margin: auto;
  float: left;
  height: 100px;
}

@media (max-width: 1024px) {
  div.page-description{
    display: grid;
    height: fit-content;
    /*
    display: none;
    */
  }
  div.page-description div{
    padding: 0 1rem 1rem 1rem;    
  }
}
@media (max-width: 512px) {
  div.page-description{
    font-size: 12px;
    display: grid;
    height: fit-content;
    /*
    display: none;
    */
  }
  div.page-description img{
    display: none;
  }
  
}
</style>