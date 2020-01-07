<template>
  <v-app>

    <Menu/>
    <v-content>
      <router-view/>
    </v-content>

  </v-app>
</template>

<script>
import Menu from './components/Menu';

export default {
  name: 'App',

  components: {
    Menu
  },

  data: () => ({
  }),
};
</script>

<style>
  .v-fade-enter-active{
    transition: all .8s ease;
  }
  .v-fade-leave-active {
    transition: all .20s cubic-bezier(.17, .67, .83, .67);
  }
  .v-fade-enter, .v-fade-leave-to {
    transform: translateY(800px);
    opacity: 0;
  }
</style>

