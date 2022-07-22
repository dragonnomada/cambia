<template>
    <div class="bot-hello">
        <div class="bot-message">
            <div class="flex-wrapper-one">
                <p class="message-text">
                    ¡Hola!
                    <div class="bot-hello-icon">
                        <span class="icon"><i class="fa-regular fa-face-smile"></i></span>
                        <span class="icon floating"><i class="fa-solid fa-heart"></i></span>
                    </div>
                </p>
            </div>
        </div>
    </div>
</template>

<style scoped>
.bot-hello {
    display: flex;
}

.bot-hello-icon {
    position: relative;
    padding-left: 6px;
}

.bot-hello-icon > .floating {
    color: crimson;
    zoom: 0.5;
    position: absolute;
    right: -8px;
    top: -8px;
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
    font-size: 14px;
    font-weight: 600;
    line-height: normal;
    color: #3F3FB8;
}
</style>