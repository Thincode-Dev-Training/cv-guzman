<template>
  <v-container grid-list-md>
    <v-layout row wrap>
      <v-flex xs12>
        <v-card>
          <v-card-title class="front">
            <h2 class="headline font-weight-light mb-4">Knowledge</h2>
          </v-card-title>
          <br>
          <v-list two-line>
            <template v-for="(item, index) in items">
              <v-divider v-if="item.divider" :key="index" :inset="item.inset"></v-divider>
              <v-list-item v-else :key="item.title">
                <v-icon :color="item.color">{{item.avatar}}</v-icon>
                <v-list-item-content>
                  <v-list-item-title v-html="item.title"></v-list-item-title>
                  <v-list-item-subtitle v-html="item.subtitle"></v-list-item-subtitle>
                </v-list-item-content>
                 <v-rating
                  :key="index"
                  :value="item.value"
                  color="orange"
                  background-color="orange"
                  class="mr-2"
                  ></v-rating>
              </v-list-item>
            </template>
          </v-list>
        </v-card>
      </v-flex>
    </v-layout>

    <v-layout row wrap>
      <v-flex xs12 sm6>
        <v-card>
          <v-card-title class="front">
            <h2 class="headline font-weight-light mb-4">Languages</h2>
          </v-card-title>
          <br>
          <v-card-text class="text-center">
            <template v-for="(len, index) in lengu">
              <span :key="index">{{len.title}}</span>
              <v-progress-linear
              :key="index"
              :color="len.color"
              height="10"
              :value="len.value"
              striped
              ></v-progress-linear>
              <br :key="index">
            </template>
            <br>
          </v-card-text>
        </v-card>
      </v-flex>

      <v-flex xs12 sm6>
        <v-card>
          <v-card-title class="front">
            <h2 class="headline font-weight-light mb-4">Soft Skills</h2>
          </v-card-title>
          <br>
          <v-card-text class="text-center">
            <template v-for="(skill, index) in skills">
              <span :key="index">{{skill.title}}</span>
              <br :key="index">
            </template>
          </v-card-text>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
  export default {
    data: () => ({
      items: [
        { avatar: 'mdi-alpha-c-circle', title: 'C++', color: 'blue',
        subtitle: "", value: "4"},
        { divider: true, inset: true },
        { avatar: 'mdi-language-python', title: 'Python', color: 'green',
        subtitle: "", value: "2"},
        { divider: true, inset: true },
        { avatar: 'mdi-ruby', title: 'Ruby', color: 'red',
        subtitle: "Ruby on Rails / Rspec / VueJS", value: "3"},
        { divider: true, inset: true },
        { avatar: 'mdi-language-javascript', title: 'JavaScript', color: 'orange',
        subtitle: "JQuery", value: "3"},
        { divider: true, inset: true },
        { avatar: 'mdi-database', title: 'DataBase', color: 'blue',
        subtitle: "Relational database management", value: "4"},
        { divider: true, inset: true },
        { avatar: 'mdi-arrow-decision', title: 'Agile Methodologies', color: 'purple',
        subtitle: "Scrum / Kanba Knowledge", value: "3"}
      ],
      skills: [
        {title: 'Leadership'},
        {title: 'Teamwork'},
        {title: 'Continuous Learning'},
        {title: 'Vision'},
        {title: 'Tolerance to frustration'},
        {title: 'Quality'}
      ],
      lengu: [
        {title: 'Spanish', color: 'light-blue', value: '100'},
        {title: 'English', color: 'light-green', value: '70'},
      ]
    }),
  }
</script>