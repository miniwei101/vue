<script setup>
import SpringFruit from './springFruit.vue';
import SummerFruit from './summerFruit.vue';
import { ref } from 'vue';
const threee=[
    '8888888888888',
    '0',
    '0'
];
</script>

<template>
  <div v-for="(f,i) in threee" :key="i" class="mytext">
    <p>{{i+"------>"+f}}</p>
  </div>>
</template>

<style>
.mytext{
    animation:imgInfo 5s ease-in-out;
}
@keyframes imgInfo{
    0%{
        opacity: 0;
        transform: translateY(50);
    }
    100%{
        opacity: 1;
        transform: translateY(0);
    }
}
</style>

