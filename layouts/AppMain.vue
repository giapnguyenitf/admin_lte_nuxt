<template>
  <div class="content-wrapper">
    <transition name="fade-transform" mode="out-in">
      <nuxt></nuxt>
    </transition>
  </div>
</template>
<style>
.content-wrapper {
  min-height: 800px;
}
</style>
