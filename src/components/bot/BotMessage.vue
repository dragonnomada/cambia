<template>
    <div class="bot-message">
        <div class="flex-wrapper-one">
            <p class="message-text">
                <slot></slot>
            </p>
        </div>
    </div>
</template>

<script setup>
</script>

<style lang="scss" scoped>
.bot-message {
    padding-bottom: 12px;
}

.flex-wrapper-one {
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