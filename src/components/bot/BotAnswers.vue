<template>
    <div class="bot-answers">
        <template v-for="question in props.questions">
            <div class="bot-message">
                <div class="flex-wrapper-one">
                    <p class="message-text">
                        {{ question }}
                    </p>
                </div>
            </div>
        </template>
    </div>
</template>

<script setup>
const props = defineProps({
    questions: {
        type: Array,
        default: []
    }
})
</script>

<style scoped>
.bot-answers {
    display: flex;
    flex-wrap: wrap;
}

.bot-message {
    padding-right: 12px;
    padding-bottom: 12px;
}

.flex-wrapper-one {
    background-color: #ECECFF;
    border-radius: 48px;
    box-shadow: 2px 2px 2px 0 rgba(0, 0, 0, 0.35);
    display: flex;
    align-items: center;
    padding: 0px 24px;
}

.message-text {
    font-family: "Roboto";
    font-size: 12px;
    font-weight: 600;
    line-height: normal;
    color: #3F3FB8;
}
</style>