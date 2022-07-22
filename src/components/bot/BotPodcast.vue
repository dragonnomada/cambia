<template>
    <div class="bot-podcast">
        <h1>Crea tu primer empresa</h1>
        <div class="podcast-user">
            <img alt="" class="user-avatar"
                src="https://randomuser.me/api/portraits/women/11.jpg" />
            <div class="podcast-controls">
                <div class="podcast-info">
                    <p class="user-text">
                        Victoria Ortiz <strong class="user-text-emphasis-1">Guadalajara</strong>
                    </p>
                </div>
                <div class="podcast-player">
                    <audio controls>
                        <source src="https://www.w3schools.com/html/horse.ogg" type="audio/ogg">
                        <source src="https://www.w3schools.com/html/horse.mp3" type="audio/mpeg">
                        Your browser does not support the audio element.
                    </audio>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
</script>

<style scoped>
.bot-podcast {
    margin: 0px -24px 12px -24px;
    padding: 12px 12px 24px 12px;
    background-color: rgba(63, 63, 184, 0.1);
}

.podcast-user {
    display: flex;
    align-items: center;
}

.user-avatar {
    width: 64px;
    height: 64px;
    margin-right: 6px;
    border-radius: 50%;
    object-fit: cover;
}

audio {
    zoom: 0.8;
}

p {
    margin: 0px;
    padding: 0px 12px 6px 12px;
}

.user-text {
    font-family: "Roboto";
    font-size: 12px;
    font-weight: 600;
    line-height: normal;
    color: rgba(12, 11, 11, 1);
}

.user-text-emphasis-1 {
    font-family: "Roboto";
    font-size: 9px;
    font-weight: 400;
    line-height: normal;
    color: rgba(12, 11, 11, 1);
}
</style>