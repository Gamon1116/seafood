<template>
  <div id="material-kit">
    <div :class="{ 'nav-open': NavbarStore.showNavbar }">
      <router-view name="header" />
      <div>
        <!-- 여긴 home.vue -->
        <router-view />
      </div>
      <router-view name="footer" />
    </div>
  </div>

</template>

