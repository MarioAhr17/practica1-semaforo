<template>
  <div>
    <div class="semaforo">
      
      <div class="circle" :style="{ backgroundColor: currentColor === 'rojo' ? 'red' : 'black' }"></div>
      
      <div class="circle" :style="{ backgroundColor: currentColor === 'amarillo' ? 'yellow' : 'black' }"></div>
      
      <div class="circle" :style="{ backgroundColor: currentColor === 'verde' ? 'green' : 'black' }"></div>
    
    <select v-model="currentColor">
      <option value="rojo">Rojo</option>
      <option value="amarillo">Amarillo</option>
      <option value="verde">Verde</option>
    </select>
    </div>
  </div>
  <NuxtLink to="/">
        inicio
  </NuxtLink>
</template>

<script setup>
import { ref } from 'vue'


const currentColor = ref('rojo')
</script>

<style
 props>
.semaforo {
  width: 100px;
  height: 300px;
  background-color: gray;
  padding: 10px;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
  border-radius: 10px;
}

.circle {
  width: 60px;
  height: 60px;
  border-radius: 50%;
  background-color: black;
}

select {
  margin-bottom: 20px;
}
</style>
