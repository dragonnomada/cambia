<template>
  <div class="bot-inline">
    <img
      alt=""
      class="bot-icon"
      src="https://static.overlay-tech.com/assets/993ae741-856e-472d-80f7-e579fd8d8866.svg"
    />
    <div class="flex-wrapper-one">
      <p class="message-text">
        <slot></slot>
      </p>
    </div>
  </div>
</template>

<script setup>
</script>

<style lang="scss" scoped>
.bot-inline {
  display: flex;
  align-items: center;
  padding: 12px 24px 12px 24px;
}
.bot-icon {
  width: 38px;
  height: 38px;
  margin-right: 12px;
  border: 1px solid #3F3FB7;
  border-radius: 50%;
}
.flex-wrapper-one {
  background-color: #ECECFF;
  border-radius: 28px;
  box-shadow: 2px 2px 2px 0 rgba(0, 0, 0, 0.35);
  display: flex;
  align-items: center;
  padding: 0px 12px;
}
.message-text {
  font-family: "Roboto";
  font-size: 12px;
  font-weight: 400;
  line-height: normal;
  color: #3F3FB8;
}
</style>