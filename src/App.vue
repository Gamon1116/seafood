<template>
  <div id="material-kit">
    <div :class="{ 'nav-open': NavbarStore.showNavbar }">
      <router-view name="header" />
      <div>
        <!-- 여긴 index.vue -->
        <router-view />
      </div>
      <router-view name="footer" />
    </div>
  </div>

</template>

