<template>
  <div>
    <p v-bind:class="titleclass">
    Hallo, nama saya Raka Sandheo Rambani
    </p>
    <h3 v-bind:class="titleclass">
    saya berasal dari 4.G. ini adalah tugas praktikum PBK yang ke2  </h3>

    <h1>Event Listener</h1>
    <button @click="changeColor">Change Color</button>
    <div :style="{ backgroundColor: bgColor, padding: '10px' }">{{ message }}</div>

  </div>

</template>

<script setup>
import { ref, reactive } from 'vue'

const titleclass = ref("class")

const message = ref('Klik tombol di atas untuk mengubah warna!');
const bgColor = ref('black'); 

const changeColor = () => {
  bgColor.value = '#' + Math.floor(Math.random()*16777215).toString(16);
};
</script>

<style scoped>
.class {
  font-size: 25px;
  color:rgb(235, 232, 233);
}
</style>