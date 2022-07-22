<template>
    <div class="bot-hashes">
        <template v-for="tag in props.tags">
            <div class="bot-message">
                <div class="flex-wrapper-one">
                    <p class="message-text">
                        #{{ tag }}
                    </p>
                </div>
            </div>
        </template>
    </div>
</template>

<script setup>
const props = defineProps({
    tags: {
        type: Array,
        default: []
    }
})
</script>

<style scoped>
.bot-hashes {
    display: flex;
    flex-wrap: wrap;
}

.bot-message {
    padding-right: 12px;
    padding-bottom: 12px;
}

.flex-wrapper-one {
    background-color: #E0E1FF;
    border-radius: 12px;
    display: flex;
    align-items: center;
    padding: 0px 24px;
}

.message-text {
    font-family: "Roboto";
    font-size: 10px;
    font-weight: 400;
    line-height: normal;
    color: #3F3FB8;
}
</style>