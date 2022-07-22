<template>
    <div class="signin-logo">
        <div class="signin-logo-curculo-mayor"></div>
        <div class="signin-logo-curculo-menor"></div>
        <img alt="" class="signin-logo-corazones"
            src="https://static.overlay-tech.com/assets/9430a984-8453-48e7-b0ce-91f4a217605e.svg" />
    </div>
</template>

<style scoped>
.signin-logo {
    width: 38px;
    height: 38px;
    position: relative;
}

.signin-logo-curculo-mayor {
    width: 100%;
    height: 100%;
    background-color: rgba(255, 255, 255, 0.15);
    border-radius: 50%;
    position: absolute;
    left: 0px;
    top: 0px;
}

.signin-logo-curculo-menor {
    width: 70%;
    height: 70%;
    background-color: rgba(255, 255, 255, 0.35);
    border-radius: 50%;
    position: absolute;
    left: 15%;
    top: 15%;
}

.signin-logo-corazones {
    width: 26.46px;
    height: 16.72px;
    position: absolute;
    left: calc(50% - 13.23px);
    top: calc(50% - 8.36px);
}
</style>