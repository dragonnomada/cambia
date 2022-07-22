<template>
    <div class="bot-video">
        <iframe width="560" height="315" src="https://www.youtube.com/embed/d7Jye1UypAw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>
</template>

<script setup>
</script>

<style scoped>
.bot-video {
    display: flex;
    flex-direction: column;
    justify-content: center;

    margin: 0px -24px 12px -24px;
    background-color: rgba(63, 63, 184, 1);
}

iframe {
    width: 100%;
    height: 240px;
}
</style>