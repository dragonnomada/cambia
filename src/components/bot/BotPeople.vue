<template>
    <div class="bot-people">
        <template v-for="i in [1, 2]">
            <BotUser />
        </template>
    </div>
</template>

<script setup>
import BotUser from './BotUser.vue';
</script>

<style scoped>
.bot-people {
    display: flex;
    flex-wrap: wrap;
    padding: 0px 12px;
}
</style>