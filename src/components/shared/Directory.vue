<script setup>
const props = defineProps({
  items:Array
});

//console.log(props.items);
</script>

<template>
  <div class="directory">
    <h3>目录</h3>
    <hr />
    <ol>
      <li v-for="item of props.items">
        <a :href="item.href">{{ item.name }}</a>
      </li>
    </ol>
  </div>
  <br />
</template>

<style scoped>
div.directory{
    width:fit-content;
    height: fit-content;

    background-color: var(--color-background-description);

    border:1px solid var(--color-border);

    padding: 10px 25px 10px 15px;

    font-size: small;
}

div.directory a:link,
div.directory a:visited{
  color: var(--color-text);
  text-decoration: none;
}
</style>