<script setup>
import SpringFruit from './springFruit.vue';
import SummerFruit from './summerFruit.vue';
import s0601 from './060101.vue';
import s060102 from './060102.vue';
import { ref } from 'vue';
const season='這個季節最好吃的4~~';
const onSale='西瓜小姐';

//單向綁定
const fruitName='vdd';
const fruitPrice=-111;
const fruitQuenty=111;
//雙向綁定
const fruitName2=ref('');
const fruitPrice2=ref('0');
const fruitQuenty2=ref('0');
</script>

<template>
  <h1>welcome to my fruit stand</h1>
  <h3>{{season}}</h3>
  <p>{{onSale}}</p>
  <p><span v-html="onSale"></span></p>
  <img src="fruit/apple.jpg"/>
  <SpringFruit></SpringFruit>
  <SummerFruit></SummerFruit>
  <s0601></s0601>
  <s060102></s060102>
  
  <input type="text" v-model="fruitName2"/><!-- :'three.fruitName' -->
  <input type="number" v-model="fruitPrice2"/>
  <input type="number" v-model="fruitQuenty2"/>
  
  <p>{{fruitName2}}</p>
  <p>{{fruitPrice2}}</p>
  <p>{{fruitQuenty2}}</p>
</template>

<style>
img{
    border-radius: 25%;
    width: 200px;
}
</style>
