<template>
    <div class="bot-message-container">
        <div class="bot-message">
            <div class="flex-wrapper-one">
                <p class="message-text">
                    <slot></slot>
                </p>
            </div>
        </div>
    </div>
</template>

<script setup>
</script>

<style lang="scss" scoped>
@keyframes fadeIn {
    0% {
        opacity: 0;
    }

    100% {
        opacity: 1;
    }
}

.bot-message-container {
    display: flex;
}

.bot-message {
    padding-bottom: 12px;
    animation: fadeIn 600ms;
}

.flex-wrapper-one {
    min-width: 40px;
    display: flex;
    justify-content: center;

    background-color: rgba(241, 241, 241, 1);
    border-radius: 18px;
    box-shadow: 2px 2px 2px 0 rgba(0, 0, 0, 0.35);
    display: flex;
    align-items: center;
    padding: 0px 12px;
}

.message-text {
    font-family: "Roboto";
    font-size: 14px;
    font-weight: 400;
    line-height: normal;
    color: rgba(0, 0, 0, 1);
}
</style>