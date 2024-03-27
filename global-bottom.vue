<!-- global-bottom.vue -->
<template>
  <div v-if="$slidev.nav.currentPage !== 1">
    <div class="absolute bottom-0 left-1 p-1">Créer son Twitch perso</div>
    <div class="absolute bottom-0 right-0 p-2 bottom-right">
      <SlideCurrentNo />
    </div>
  </div>
</template>

<style>
.bottom-right {
  z-index: 100;
}
</style>