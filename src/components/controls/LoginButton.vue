<template>
    <div class="button-container">
        <div class="button">
            <div class="button-icon-container">
                <img alt="" class="button-icon"
                    :src="props.picture" />
                <span class="button-text">
                    {{ props.text }}
                </span>
            </div>
        </div>
    </div>
</template>

<script setup>
const props = defineProps({
    picture: {
        type: String
    },
    text: {
        type: String,
        default: "Continuar"
    },
})
</script>

<style scoped>
.button-container {
    padding-bottom: 12px;
}

.button {
    width: 200px;
}

.button-text {
    font-family: "Roboto";
    font-size: 12px;
    font-weight: 500;
    line-height: normal;
    color: rgba(74, 74, 74, 0.75);
    display: flex;
    text-shadow: 3px 3px 3px rgba(234, 234, 234, 0.25);
    padding: 0px 12px;
}

.button-icon-container {
    display: flex;
    align-items: center;

    background-color: rgba(125, 125, 253, 0.15);
    border-radius: 18px;
    padding: 12px;
    box-shadow: 3px 3px 3px 0 rgba(234, 234, 234, 0.25),
        0 4px 4px 0 rgba(0, 0, 0, 0.25);
}

.button-icon {
    height: 18px;
}
</style>