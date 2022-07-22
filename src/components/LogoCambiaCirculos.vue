<template>
  <div class="logo-cambia-circulos">
    <div class="logo-inicio-circulo-mayor"></div>
    <div class="logo-inicio-circulo-menor"></div>
    <img
      alt=""
      class="logo-cambia"
      src="https://static.overlay-tech.com/assets/91a214c4-3feb-41a6-bf22-bf7927609828.svg"
    />
  </div>
</template>

<script>
export default {
  name: "LogoCambiaCirculos"
};
</script>

<style scoped>
.logo-cambia-circulos {
  width: 288px;
  height: 288px;
  position: relative;
}
.logo-inicio-circulo-mayor {
  width: 100%;
  height: 100%;
  background-color: rgba(255, 255, 255, 0.15);
  border-radius: 50%;
  position: absolute;
  left: 0px;
  top: 0px;
}
.logo-inicio-circulo-menor {
  width: 80%;
  height: 80%;
  background-color: rgba(255, 255, 255, 0.55);
  border-radius: 50%;
  position: absolute;
  left: 10%;
  top: 10%;
}
.logo-cambia {
  width: 70%;
  height: 60px;
  position: absolute;
  left: 15%;
  top: calc(50% - 30px);
}
</style>