<template>
  <v-app>
    <v-main>
      <app-root/>
    </v-main>
  </v-app>
</template>

<script lang="ts">
import Vue from 'vue';
import AppRoot from "@/components/Root.vue";

export default Vue.extend({
  name: 'App',

  components: {
    AppRoot,
  },

  data: () => ({
    //
  }),
});
</script>
