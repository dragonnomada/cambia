<template>
    <div class="bot-container">
        <CambiaDock />
        <div class="bot-feed">
            <BotHello />
            <BotMessage>
                ¿Estás lista para aprender nuevas habilidades el día de hoy?
                <span class="icon"><i class="fa-solid fa-user-astronaut"></i></span>
                <span class="icon"><i class="fa-solid fa-graduation-cap"></i></span>
                <span class="icon"><i class="fa-solid fa-book"></i></span>
            </BotMessage>
            <BotVideo/>
            <BotMessage>
                ¿Ya has escuchado las <strong>pláticas</strong> del día?
            </BotMessage>
            <BotPodcast/>
            <BotInline>
                Buscar más contenido como este
            </BotInline>
            <BotMessage>
                ¿Tienes algún tema en mente?
            </BotMessage>
            <BotTags :tags="['Emprender', 'Negocios', 'Ventas']" />
            <BotMessage>
                ¿Quieres conocer a los <strong>mentores</strong> más populares?
            </BotMessage>
            <BotPeople />
            <BotSuggestions title="Elegir una ruta de aprendizaje"
                :options="['Crear tu propia empresa', 'Comunicación efectiva']" />
            <BotInline>
                Jimena, ella es <strong>Susana Ramírez:</strong>
            </BotInline>
            <BotPost />
            <BotMessage>
                Susana ha tenido gran éxito en la comercialización de <strong>artesanías</strong> al acercarse a sus
                clientes de manera
                personalizada
            </BotMessage>
            <BotMessage>
                ¿Quieres <strong>aprender más</strong> sobre el negocio de las artesanías?
            </BotMessage>
            <BotAnswers :questions="['Si', 'No, otro día']" />
            <BotSuggestions title="Ver otras historias del día"
                :options="['Confección de vestidos con María Sánchez', 'Mi primer consultorio con Carmen Ayala']" />
            <BotMessage>
                Hola, ¿en qué <strong>temas</strong> estás más interesada?
            </BotMessage>
            <BotAnswers :questions="['Habilidades Digitales', 'Emprender', 'Mi primer negocio', 'Finanzas básicas']" />
        </div>
        <div class="logo-citibanamex-contenedor">
            <LogoCitiBanamex />
        </div>
    </div>
</template>

<script setup>
import CambiaDock from './CambiaDock.vue';
import BotInline from './bot/BotInline.vue';
import BotPost from './bot/BotPost.vue';
import LogoCitiBanamex from './LogoCitiBanamex.vue';
import BotMessage from './bot/BotMessage.vue';
import BotAnswers from './bot/BotAnswers.vue';
import BotTags from './bot/BotTags.vue';
import BotUser from './bot/BotUser.vue';
import BotPeople from './bot/BotPeople.vue';
import BotHello from './bot/BotHello.vue';
import BotSuggestions from './bot/BotSuggestions.vue';
import BotPodcast from './bot/BotPodcast.vue';
import BotVideo from './bot/BotVideo.vue';
</script>

<style scoped>
.bot-container {
    height: 100vh;
    display: flex;
    flex-direction: column;
}

.bot-feed {
    padding: 24px 24px 96px 24px;
    overflow: auto;
}

@media screen and (min-width: 768px) {
    .bot-feed {
        padding-left: 140px;
        padding-right: 140px;
    }
}

@media screen and (min-width: 1024px) {
    .bot-feed {
        padding-left: 240px;
        padding-right: 240px;
    }
}

@media screen and (min-width: 1420px) {
    .bot-feed {
        padding-left: 480px;
        padding-right: 480px;
    }
}

.logo-citibanamex-contenedor {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    width: 100%;
    height: 60px;

    position: fixed;
    left: 0px;
    bottom: 0px;

    background-color: white;

    z-index: 100;
}
</style>