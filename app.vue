<template>
  <main class="wrapper">
    <AppMenu class="menu-left" />
    <div class="main">
      <AppHeader />
      <AppMainCart />
    </div>
  </main>
</template>

<script setup></script>

<style lang="scss">
$background-color: rgb(245, 247, 250);
$text-color: #b1b1b1;
.wrapper {
  display: flex;
  min-height: 100vh;
  background-color: $background-color;
}
.menu-left {
  flex: 1 0 205px;
  max-width: 249px;
  background-color: rgb(255, 255, 255);
  color: #fff;
  border-right: 1px solid rgb(230, 239, 245);
}
.main {
  flex: 1;
}
</style>
