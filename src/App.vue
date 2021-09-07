<template>
  <v-app>
    <v-main>
      <KeyboardHero/>
    </v-main>
  </v-app>
</template>

<script>
import KeyboardHero from "./views/KeyboardHero";

export default {
  name: 'App',

  components: {
    KeyboardHero,
  },

  data: () => ({
    //
  }),
};
</script>
