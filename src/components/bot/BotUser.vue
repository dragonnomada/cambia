<template>
  <div class="user">
    <img
      alt=""
      class="user-avatar"
      src="https://static.overlay-tech.com/assets/8760d872-2d27-4d9d-b542-7bda0c3fff52.png"
    />
    <p class="user-text">
      Alma Ríos<br />
      <strong class="user-text-emphasis-1"
        >Querétaro</strong
      >
    </p>
  </div>
</template>

<script setup>
</script>

<style lang="scss" scoped>
.user {
  display: flex;
  align-items: center;
  padding-right: 12px;
  padding-bottom: 12px;
}
.user-avatar {
  width: 42px;
  height: 42px;
  margin-right: 6px;
  border-radius: 50%;
  object-fit: cover;
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