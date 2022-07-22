<template>
    <div class="contenedor">
        <LogoCambiaCirculos/>
        <div class="separador"></div>
        <div class="logo-citibanamex-contenedor">
            <LogoCitiBanamex/>
        </div>
    </div>
</template>

<script setup>
import LogoCambiaCirculos from './LogoCambiaCirculos.vue';
import LogoCitiBanamex from './LogoCitiBanamex.vue';</script>

<style scoped>
.contenedor {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    width: 100%;
    height: 100%;
    background: linear-gradient(#0404A9 10%, rgba(80, 41, 216, 0.7) 35%, rgba(205, 21, 143, 0) 90%);
}

.separador {
    padding: 48px;
}

.logo-citibanamex-contenedor {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    width: 100%;
    height: 15%;

    position: absolute;
    left: 0px;
    bottom: 0px;
}
</style>