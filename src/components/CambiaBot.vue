<template>
    <div class="bot-container">
        <CambiaDock />
        <div class="bot-feed">
            <BotHello />

            <div v-for="child in children" :key="child.name">
                <component :is="child"></component>
            </div>

            <!--
            <BotMessage>
                ¿Estás lista para aprender nuevas habilidades el día de hoy?
                <span class="icon"><i class="fa-solid fa-user-astronaut"></i></span>
                <span class="icon"><i class="fa-solid fa-graduation-cap"></i></span>
                <span class="icon"><i class="fa-solid fa-book"></i></span>
            </BotMessage>
            <BotVideo />
            <BotMessage>
                ¿Ya has escuchado las <strong>pláticas</strong> del día?
            </BotMessage>
            <BotPodcast />
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
            -->
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
import { h, onMounted, ref } from 'vue';

const children = ref([])

async function sleep(milliseconds = 600) {
    return await new Promise(resolve => {
        setTimeout(resolve, milliseconds)
    })
}

async function insertComponent(component) {
    children.value.push(h(BotMessage, {}, "..."))
    await sleep(900)
    children.value.pop()
    await sleep(200)
    children.value.push(component)
}

function createMessage(content) {
    return h(BotMessage, {}, h("div", {
        innerHTML: content
    }))
}

async function insertMessage(content) {
    await insertComponent(createMessage(content))
}

// <BotMessage>
//    ¿Tienes algún tema en mente?
// </BotMessage>
// <BotTags :tags="['Emprender', 'Negocios', 'Ventas']" />

function createInlineMessage(content) {
    return h(BotInline, {}, h("div", {
        innerHTML: content
    }))
}

async function insertInlineMessage(content) {
    await insertComponent(createInlineMessage(content))
}

onMounted(async () => {
    await insertMessage(`¿Estás lista para aprender nuevas habilidades el día de hoy?
            <span class="icon"><i class="fa-solid fa-user-astronaut"></i></span>
            <span class="icon"><i class="fa-solid fa-graduation-cap"></i></span>
            <span class="icon"><i class="fa-solid fa-book"></i></span>`)

    await sleep(2000)

    await insertMessage("Comecemos escuchando esta historia que estoy seguro que te podría gustar")

    await insertComponent(h(BotPodcast))

    await sleep(20000)

    await insertInlineMessage("Buscar más contenido como este")

    await sleep(2000)

    await insertMessage("¿Te ha gustado esta historia?")

    await insertComponent(h(BotAnswers, {
        questions: ['Sí', 'No mucho']
    }))

    await sleep(3000)

    children.value = []
    
    await insertMessage(`Vamos a buscar nuevo contenido <span class="icon"><i class="fa-solid fa-face-laugh-beam"></i></span>`)

    await insertComponent(h(BotTags, {
        tags: ['Emprender', 'Negocios', 'Ventas']
    }))

    await sleep(2000)

    await insertComponent(h(BotVideo))

    await sleep(1200)

    await insertComponent(h(BotSuggestions, {
        title: "Ver otras historias del día",
        options: ['Habilidades Digitales', 'Emprender', 'Mi primer negocio', 'Finanzas básicas']
    }))

    
})
</script>

<style scoped>
.bot-container {
    height: 100vh;
    display: flex;
    flex-direction: column;
}

.bot-feed {
    display: flex;
    flex-direction: column;

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