<template>
    <div class="cambia-dock">
        <div class="cambia-dock-rect1"></div>
        <div class="cambia-dock-rect2"></div>
        <div class="cambia-dock-logo">
            <LogoCambiaCorazonesSmall/>
            <img alt="" class="cambia-dock-logo-text"
                src="https://static.overlay-tech.com/assets/6e27885f-ebfe-4ee1-9edb-c268f68b467a.svg" />
        </div>
    </div>
</template>

<script setup>
import LogoCambiaCorazonesSmall from './LogoCambiaCorazonesSmall.vue';
</script>

<style lang="scss" scoped>
.cambia-dock {
    padding: 6px 0 0;
    position: relative;
}

.cambia-dock-rect1 {
    width: 100%;
    height: 64px;
    background-color: rgba(63, 63, 184, 1);
    border-radius: 0px 0px 25px 25px;
    position: absolute;
    left: 0;
    top: 0;
}

.cambia-dock-rect2 {
    width: 100%;
    height: 70px;
    background-color: rgba(192, 192, 192, 1);
    border-radius: 0px 0px 25px 25px;
    position: relative;
    z-index: -1;
}

.cambia-dock-logo {
    display: flex;
    align-items: center;
    position: absolute;
    left: 11px;
    top: 13px;
}

.cambia-dock-logo-text {
    width: 100.84px;
    height: 20.47px;
    padding-left: 3px;
}
</style>