<script>
import AppHeader from './AppHeader.vue';
import AppMain from './AppMain.vue';
import { store } from './assets/data/store';
import { api } from './assets/data/index';
export default {
  name: 'Boolflix',
  components: { AppHeader, AppMain }
}
</script>

<template>
  <AppHeader />
  <AppMain />
</template>

<style></style>
