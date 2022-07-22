<template>
    <div class="bot-post-container">
        <div class="bot-post">
            <img class="bot-post-image"
                src="https://static.overlay-tech.com/assets/fd167405-95b6-4bd4-a1f5-aef161e44c76.png" />
            <img alt="" class="bot-post-icon"
                src="https://static.overlay-tech.com/assets/6f943061-dfdd-48d3-9563-b89e78eebddd.svg" />
            <p class="bot-post-text">
                Comercialización de artesanías
            </p>
        </div>
    </div>
</template>

<script setup>
</script>

<style lang="scss" scoped>
.bot-post-container {
    padding-bottom: 12px;
}

.bot-post {
    border-radius: 25px;
    padding: 100px 44px 0px 10px;
    display: flex;
    align-items: flex-start;
    position: relative;
    background-color: red;
    overflow: hidden;
}

.bot-post-image {
    width: 100%;
    height: 100%;
    position: absolute;
    left: 0px;
    top: 0px;
    object-fit: cover;
}

.bot-post-icon {
    width: 24px;
    height: 24px;
    margin-right: 11px;
    margin-top: 24px;
    z-index: 1;
}

.bot-post-text {
    width: 86.79%;
    font-family: "Roboto";
    font-size: 26px;
    font-weight: 700;
    line-height: normal;
    color: rgba(255, 255, 255, 1);
    align-self: stretch;
    display: flex;
    z-index: 1;
}

@media screen and (min-width: 480px) {
    .bot-post {
        padding: 240px 44px 0px 10px;
    }
}
</style>