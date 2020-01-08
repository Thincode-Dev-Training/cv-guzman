<template>
  <v-container grid-list-md>
    <v-card-title class="front">
      <h2 class="headline font-weight-light mb-4">Complementary data</h2>
    </v-card-title>
    <v-card-text class="text-center">
      <template v-for="(extra,index) in extras">
        <br :key="index">
        <v-icon :color="extra.color" :key="index">{{extra.icono}}</v-icon>
        <span :key="index">{{extra.title}}</span>
        <br :key="index">
      </template>
    </v-card-text>
  </v-container>
</template>

<script>
export default {
  //
}
</script>