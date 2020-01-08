<template>
  <v-container grid-list-md>
    <v-layout row wrap>
      <template v-for="(item, index) in items">
        <v-flex xs12 sm6 :key="index">
          <v-card>
            <v-card-title class="front">
              <h2 class="headline font-weight-light mb-4">{{item.name}}</h2>
            </v-card-title>
            <br>
            <v-card-text class="text-center">
              <v-icon color="purple darken-2">mdi-school</v-icon>
              <p>{{item.title}}</p>
              <v-icon color="orange darken-2">mdi-calendar-multiple</v-icon>
              <p>{{item.date}}</p>
              <v-icon color="blue darken-3">mdi-medal</v-icon>
              <p>{{item.activity}}</p>
            </v-card-text>
          </v-card>
        </v-flex>
      </template>
    </v-layout>
  </v-container>
</template>


<script>
  export default {
    data: () => ({
      items: [
        {name: 'Universidad de Guanajuato', title: 'Computer Systems Engineering', date: '2015 - 2019', activity: '2019 - Work on Analysis of dynamic scenes for motion detection in Summer Research at the Universidad de Guanajuato, in which a vision system was configured using a RGB-D sensor to capture color images (RGB) anddepth(D)'},
        {name: 'CECyTEG', title: 'Technician in Support and Maintenance to Computer equipment', date: '2011 - 2014', activity: ""}
      ]
    }),
  }
</script>