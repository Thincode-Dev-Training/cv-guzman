<template>
  <v-container>
    <v-toolbar app flat style="background: transparent">
      <v-app-bar-nav-icon @click="drawer = !drawer">
        <v-icon>mdi-view-list</v-icon>
      </v-app-bar-nav-icon>
      <v-toolbar-title>MyCV</v-toolbar-title>
    </v-toolbar>

    <v-navigation-drawer app v-model="drawer">
      <v-img src="@/assets/offi.jpg" height="100%">
        <template>
          <v-list>
            <v-list-item>
              <v-list-item-avatar>
                <v-img src="@/assets/mjgv.jpeg"></v-img>
              </v-list-item-avatar>
            </v-list-item>

            <v-list-item link :to="{name: 'home'}">
              <v-list-item-content>
                <v-list-item-title class="title">María Guzmán</v-list-item-title>
                <v-list-item-subtitle>Computer Stystems Engineer</v-list-item-subtitle>
              </v-list-item-content>
            </v-list-item>
          </v-list>
        </template>

        <v-divider></v-divider>

        <v-list nav>
          <v-list-item link :to="{name: 'education'}">
            <v-list-item-icon>
              <v-icon>mdi-book-open-page-variant</v-icon>
            </v-list-item-icon>
            <v-list-item-title> Education</v-list-item-title>
          </v-list-item>
          <v-list-item link :to="{name: 'skills'}">
            <v-list-item-icon>
              <v-icon>mdi-folder-star</v-icon>
            </v-list-item-icon>
            <v-list-item-title> Skills</v-list-item-title>
          </v-list-item>
          <v-list-item link :to="{name: 'experience'}">
            <v-list-item-icon>
              <v-icon>mdi-briefcase-account</v-icon>
            </v-list-item-icon>
            <v-list-item-title> Experience</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-img>
    </v-navigation-drawer>
  </v-container>
</template>


<script>
  export default {
    name: 'Menu',

    data: () => ({
      drawer: true
    }),
  };
</script>
