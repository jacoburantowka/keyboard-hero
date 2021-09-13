<template>
  <v-container>
    <KeyboardHero/>
  </v-container>
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

<style>
body {
  background-color: rgba(0, 0, 0, 0.9);
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-weight: 500;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
}
</style>