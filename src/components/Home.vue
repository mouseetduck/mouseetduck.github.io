<script setup>
//import SupportIcon from './icons/IconSupport.vue'
import { ref } from 'vue'
import Description from '@/components/shared/Description.vue'
import Directory from '@/components/shared/Directory.vue'
import ImgFcyzUrl from './images/Icon-fcyz.png'

const dir = ref([
  {
    name:"1",
    href:"#",
  },
  {
    name:"2",
    href:"#",
  },
  {
    name:"3",
    href:"#",
  },
  {
    name:"4",
    href:"#",
  }
])

</script>

<template>

  <div class="greetings">
    <h1>欢迎来到肥城一中!</h1>
    <hr />
    <h3>>>>Welcome to No.1 High School of Feicheng!</h3>
  </div>  
  <br />

  <!--Description start-->
  <Description :url="ImgFcyzUrl">
    <template #heading><p>本页是关于<b>肥城一中</b>的介绍</p></template>
  </Description>
  <!--Description end-->

  <!--Directory start-->
  <Directory :items = dir />
  <!--Directory end-->

  <!--Main start-->
  <main>
    <h2>介绍</h2>
    <hr />
    <h3>官方(?)</h3>
    <p>肥城市第一高级中学（简称肥城一中）是中国山东省肥城市的一所公立高中，始建于1952年（原名山东省肥城中学），1979年迁入新城，现校址位于肥城市文化路010号，目前学校占地122亩，总建筑面积9.6万平方米，近年来绿化面积不断减少。学校共设72个教学班级，学生约4000人，教职工大约350人，多年高考成绩居肥城市第一，被评为省级示范高中。</p>
    <!--
    <h3>事实上。。。</h3>
    <ul>
      <li><del>食堂不尽人意</del></li>
      <li><del>寝室一言难尽</del></li>
      <li><del>厕所门质量。。。</del>(不知道修好了吗)</li>
      <li><del>收费多如牛毛</del></li>
    </ul>
    <br />
  -->
  </main>
  <!--Main end-->

</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 2.6rem;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1 {
  margin-bottom: 0;
  text-align: center;
}
.greetings h3 {
  position: relative;
  left: 25px;
  margin-top: 0;
  text-align: center;
}

main{

}

main p{
  font-size: medium;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>
