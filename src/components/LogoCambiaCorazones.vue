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
    width: 175px;
    height: 175px;
    position: relative;
}

.signin-logo-curculo-mayor {
    width: 100%;
    height: 100%;
    background-color: rgba(229, 228, 228, 0.45);
    border-radius: 50%;
    position: absolute;
    left: 0px;
    top: 0px;
}

.signin-logo-curculo-menor {
    width: 70%;
    height: 70%;
    background-color: rgba(26, 26, 172, 0.15);
    border-radius: 50%;
    position: absolute;
    left: 15%;
    top: 15%;
}

.signin-logo-corazones {
    width: 120px;
    height: 78px;
    position: absolute;
    left: calc(50% - 60px);
    top: calc(50% - 39px);
}
</style>