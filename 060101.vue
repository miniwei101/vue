<script setup>
import SpringFruit from './springFruit.vue';
import SummerFruit from './summerFruit.vue';
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

const visibleString=ref('');
const springTrue=ref('SpringFruit');
const summerFalse=ref('SummerFruit');
const isVisible=ref(false);
const visibleFruit=()=>{
    //isVisible.value=!isVisible.value;
    if(isVisible)
    {visibleString.value=springTrue;isVisible.value=!isVisible.value;}
    else
    {visibleString.value=summerFalse;isVisible.value=!isVisible.value;}
    
};
</script>

<template>
  <!-- <button v-on:click="visibleFruit">{{isVisible?"000":"111"}}</button> -->
  <button v-on:click="visibleFruit">{{visibleString}}</button>
      <SpringFruit v-if="isVisible"></SpringFruit>
      <SummerFruit v-if="!isVisible"></SummerFruit>
</template>

<style>
img{
    border-radius: 25%;
    width: 200px;
}
</style>
