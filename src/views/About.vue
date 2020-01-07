<template>
  <v-container grid-list-md>
    <v-avatar slot="offset" class="mx-auto d-block" size="90">
      <img src="@/assets/whoo.jpeg">
    </v-avatar>

    <br>
    <v-divider></v-divider>
    <br>

    <v-layout row wrap text-center>
      <v-flex xs12 sm6>
        <h2>María Guzmán</h2>
        <p class="font-weight-thin">CSI</p>
        <p class="font-weight-light">Person who search to secure a position
        as a Developer or similar to use my current analytical skills
        and knowledge and develop these skills in a practical and
        accelerated environment.
        My professional objective is to take responsibility for the
        analysis and implementation of my knowledge and actively
        contribute to the overall success of any business for which I work.
        </p>
      </v-flex>
      <v-flex xs12 sm6>
        <v-icon color="blue darken-2">mdi-outlook</v-icon>
        <p class="font-weight-light">maria.guzman@thincode.com</p>
        <v-icon color="purple darken-2">mdi-cellphone-iphone</v-icon>
        <p class="font-weight-light">(+52) 456 655 60 52</p>
        <v-icon color="green darken-2">mdi-map-marker-radius</v-icon>
        <p class="font-weight-light">Valle de Santiago, Gto.</p>
        <v-icon color="orange darken-2">mdi-calendar-range</v-icon>
        <p class="font-weight-light">03/19/1996</p>
        <v-icon color="blue darken-3">mdi-linkedin</v-icon>
        <p class="font-weight-light">María José GV</p>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  //
}
</script>