<template>
  <v-app>
    <div class="app">
      <NavPage />

      <v-main>
        <Nuxt />
      </v-main>

      <FooterPage />
    </div>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
}
</script>

<style>
.app {
  background-color: white;
}
</style>
