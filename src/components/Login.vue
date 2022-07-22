<template>
    <div class="login">
        <div class="sign-logo-contenedor">
            <LogoCambiaCorazones />
        </div>
        <div class="signin-form">
            <Field name="email" placeholder="Escribe tu correo" />
            <Field name="password" placeholder="Escribe tu contraseña"
                icon="https://static.overlay-tech.com/assets/f781ad01-cb2a-4871-be6a-a048caffe55e.svg" is-password />
            <div class="remeber-forgot">
                <Check />
                <Link />
            </div>
        </div>
        <div class="signin-buttons">
            <div class="signin-main-button">
                <MainButton />
                <InfoLink />
            </div>
            <div class="signin-other-buttons">
                <LoginButton text="Continuar con Twitter"
                    picture="https://static.overlay-tech.com/assets/a05b920a-e0a4-41d8-bdaf-5c792f1346f8.svg" />
                <LoginButton text="Continuar con Gamil"
                    picture="https://static.overlay-tech.com/assets/0b0b64a5-0147-434d-8055-db52d0881bac.svg" />
                <LoginButton text="Continuar con Apple"
                    picture="https://static.overlay-tech.com/assets/f71ecb0f-0638-4a9f-b20f-f8bb6fd0741f.svg" />
                <LoginButton text="Continuar con Facebook"
                    picture="https://static.overlay-tech.com/assets/cd00e447-0c1f-4fe9-be1b-daac592439e8.svg" />
            </div>
            <div class="signin-spacer"></div>
        </div>
        <div class="logo-citibanamex-contenedor">
            <LogoCitiBanamex />
        </div>
    </div>
</template>

<script setup>
import Field from './controls/Field.vue';
import LogoCambiaCorazones from './LogoCambiaCorazones.vue';
import Check from './controls/Check.vue';
import Link from './controls/Link.vue';
import MainButton from './controls/MainButton.vue';
import InfoLink from './controls/InfoLink.vue';
import LoginButton from './controls/LoginButton.vue';
import LogoCitiBanamex from './LogoCitiBanamex.vue';
</script>

<style lang="scss" scoped>
.login {
    width: 100%;
    height: 100%;

    display: flex;
    flex-direction: column;

    background-color: rgba(255, 255, 255, 1);

    overflow: auto;
}

.sign-logo-contenedor {
    display: flex;
    justify-content: center;
    padding: 24px;
}

.signin-form {
    padding: 0px 24px;
}

.remeber-forgot {
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.signin-buttons {
    padding: 12px 36px;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.signin-main-button {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
}

.signin-other-buttons {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
}

.signin-spacer {
    width: 100%;
    height: 60px;
}

.logo-citibanamex-contenedor {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    width: 100%;
    height: 60px;

    position: absolute;
    left: 0px;
    bottom: 0px;

    background-color: white;
}

@media screen and (min-width: 480px) {
    .login {
        width: 80%;
        align-self: center;
    }
}
@media screen and (min-width: 768px) {
    .login {
        width: 60%;
        align-self: center;
    }
}

@media screen and (min-width: 1024px) {
    .login {
        width: 40%;
        align-self: center;
    }
}

@media screen and (min-width: 1280px) {
    .login {
        width: 30%;
        align-self: center;
    }
}
</style>