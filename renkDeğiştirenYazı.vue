<template>
    <div>
      <h1 :style="{ color: yazıRengi }  ">Hello World</h1>
      <button @click="renkDeğiştir" class="bg-red mt-1">Rengi Değiştir</button>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
 
  const karakterler = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9', 'a', 'b', 'c', 'd', 'e', 'f'];
  
  function rasgeleRenkKodu() {
    let renkKodu = '#';
    for (let i = 0; i < 6; i++) {
      renkKodu += karakterler[Math.floor(Math.random() * karakterler.length)];
    }
    return renkKodu;
  }
 
  const yazıRengi = ref('#000');
  

  function renkDeğiştir() {
    yazıRengi.value = rasgeleRenkKodu();
  }
  </script>



  