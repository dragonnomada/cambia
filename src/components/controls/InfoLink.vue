<template>
    <div class="registro">
        <p class="registro-existe">¿Tienes cuenta?</p>
        <p class="registro-nuevo">Registarme</p>
    </div>
</template>

<style scoped>
.registro {
    display: flex;
    align-items: flex-start;
    padding-bottom: 24px;
}

.registro-existe {
    height: 11px;
    width: 88px;
    font-family: "Roboto";
    font-size: 12px;
    font-weight: 500;
    line-height: normal;
    color: rgba(74, 74, 74, 0.75);
    display: flex;
    margin-right: 20px;
}

.registro-nuevo {
    height: 11px;
    width: 70px;
    font-family: "Roboto";
    font-size: 12px;
    font-weight: 600;
    line-height: normal;
    color: rgba(63, 63, 184, 1);
    display: flex;
}
</style>