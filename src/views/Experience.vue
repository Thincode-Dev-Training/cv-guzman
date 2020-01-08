<template>
  <v-container grid-list-md>
    <v-layout row wrap>
      <template v-for="(item,index) in items">
        <v-flex xs12 sm6 :key="index">
          <v-card>
            <v-card-title class="front">
              <h2 class="headline font-weight-light mb-4">{{item.name}}</h2>
            </v-card-title>
            <br>
            <v-card-text class="text-center">
              <v-icon color="purple darken-2">mdi-account-card-details</v-icon>
              <p>{{item.title}}</p>
              <v-icon color="orange darken-2">mdi-format-list-bulleted-type</v-icon>
              <p>{{item.activity}}</p>
              <v-icon color="blue darken-3">mdi-calendar-multiple</v-icon>
              <p>{{item.date}}</p>
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
        {name: 'Thincode', title: 'Jr Developer', date: 'August 2019 - Current',
        activity: 'Training in different tools such as Ruby on Rails, Rspec, Vue, etc. / Support in development activities within a migration project. / Support in maintaining communication with the client.'},
        {name: 'Doble Clik', title: 'Technician', date: 'June 2017 - November 2017',
        activity: 'Technical support to customers, helping to solve equipment or connection problems. / Configuration of routers, antennas and company equipment. / Route management for problem attention.'}
      ]
    }),
  }
</script>