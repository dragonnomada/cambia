<template>
    <div class="suggestions">
        <div class="suggestion-title">
            <span>{{ props.title }}</span>
        </div>
        <template v-for="option in props.options">
            <div class="button-container">
                <div class="button">
                    <p class="button-text">{{ option }}</p>
                </div>
            </div>
        </template>
    </div>
</template>

<script setup>
const props = defineProps({
    title: {
        type: String,
        default: ""
    },
    options: {
        type: Array,
        default: []
    }
})
</script>

<style scoped>
.suggestions {
    padding-top: 24px;
}

.suggestion-title {
    padding: 12px;
}
.suggestion-title > span {
    font-family: "Roboto";
    font-size: 14px;
    font-weight: 500;
    color: #717171;
}

.button-container {
    padding-bottom: 12px;
}

.button {
    width: 100%;
    background-color: rgba(63, 63, 184, 1);
    box-shadow: 5px 4px 4px 0 rgba(0, 0, 0, 0.25);
    display: flex;
    justify-content: center;
    align-items: center;
}

.button-text {
    font-family: "Roboto";
    font-size: 12px;
    font-weight: 500;
    color: white;
}
</style>