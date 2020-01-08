<template>
  <v-container>
    <v-hover v-slot:default="{ hover }">
      <v-card class="mx-auto" width="200px">

        <v-img src="@/assets/mjgv.jpeg">
          <v-expand-transition>
            <div
            v-if="hover"
            class="d-flex transition-fast-in-fast-out cyan lighten-4 v-card--reveal display-1 blue-grey-darken-4-text text-center"
            style="height: 100%"
            >
            María José Guzman Valades
            <br>
            Computer Stystems Engineer
            </div>
          </v-expand-transition>
        </v-img>
      </v-card>
    </v-hover>

    <v-container>
      <v-row align="center" justify="center">
        <v-btn fab color="pink lighten-4" href="https://google.com">
          <v-icon>mdi-instagram</v-icon>
        </v-btn>
        <div class="mx-2"></div>
        <v-btn fab color="deep-orange lighten-4" href="https://google.com">
          <v-icon>mdi-facebook</v-icon>
        </v-btn>
        <div class="mx-2"></div>
        <v-btn fab color="blue lighten-4" href="https://google.com">
          <v-icon>mdi-twitter</v-icon>
        </v-btn>
        <div class="mx-2"></div>
      </v-row>
    </v-container>

    <v-stepper v-model="e1">
      <v-stepper-items>
        <v-stepper-content step="1" class="text-center">
          <h2>María Guzmán</h2>
          <p class="font-weight-thin">CSI</p>
          <p class="font-weight-light">I'm a person who search to secure a position
          as a Developer or similar to use my current analytical skills
          and knowledge and develop these skills in a practical and
          accelerated environment.
          My professional objective is to take responsibility for the
          analysis and implementation of my knowledge and actively
          contribute to the overall success of any business for which I work.
          </p>
          <br>
          <v-btn color="deep-purple lighten-4" depressed @click="e1 = 2">Contact</v-btn>
        </v-stepper-content>

        <v-stepper-content step="2" class="text-center">
          <v-icon color="blue darken-2">mdi-outlook</v-icon>
          <p class="font-weight-light">maria.guzman@thincode.com</p>
          <v-icon color="purple darken-2">mdi-cellphone-iphone</v-icon>
          <p class="font-weight-light">(+52) 456 655 60 52</p>
          <v-icon color="green darken-2">mdi-map-marker-radius</v-icon>
          <p class="font-weight-light">Valle de Santiago, Gto.</p>
          <v-icon color="orange darken-2">mdi-calendar-range</v-icon>
          <p class="font-weight-light">03/19/1996</p>
          <v-btn icon flat href="https://www.linkedin.com/in/maria-jose-guzman-33434b17b/">
            <v-icon color="blue darken-3">mdi-linkedin</v-icon>
          </v-btn>
          <p class="font-weight-light">María José GV</p>
          <br>
          <v-btn color="deep-purple lighten-4" depressed  @click="e1 = 1">About me</v-btn>
        </v-stepper-content>
      </v-stepper-items>
    </v-stepper>
  </v-container>
</template>

<script>
export default {
  name: 'home',
  data () {
    return {
      e1: 0,
    }
  },
}
</script>

<style>
  .v-card--reveal {
    align-items: center;
    bottom: 0;
    justify-content: center;
    opacity: .5;
    position: absolute;
    width: 100%;
  }
</style>
