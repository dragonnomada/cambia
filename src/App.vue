<template>
  <template v-if="currentComponent === 'Inicio'">
    <Inicio />
  </template>
  <template v-else-if="currentComponent === 'Login'">
    <Login />
  </template>
  <template v-else>
    <CambiaBot />
  </template>

</template>

<script setup>
import { onMounted, provide, ref } from 'vue';
import Inicio from './components/Inicio.vue';
import Login from './components/Login.vue';
import CambiaBot from './components/CambiaBot.vue';

const currentComponent = ref('Inicio')

onMounted(() => {
  setTimeout(() => {
    // currentComponent.value = 'Login'
    currentComponent.value = 'CambiaBot'
  }, 1000)
})

provide('app/@selectComponent', name => {
  currentComponent.value = name
})

const fieldSelected = ref('common')

provide('field/selected', fieldSelected)
provide('field/@select', name => fieldSelected.value = name)
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:ital,wght@0,100;0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap');

html,
body {
  font-family: "Roboto";

  width: 100%;
  height: 100vh;
  margin: 0px;
  padding: 0px;
}

#app {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: stretch;
  align-items: stretch;
  overflow: hidden;
}

.icon {
  color: #3F3FB8;
  padding-right: 3px;
}
</style>