<template>
  <v-app>
    <v-navigation-drawer v-model="drawer" :rail="rail" permanent>
      <template v-slot:prepend>
        <v-list-item
          lines="two"
          prepend-avatar="https://randomuser.me/api/portraits/women/81.jpg"
          subtitle="Logged in"
          title="Jane Smith"
        ></v-list-item>
        <v-list-item>

        </v-list-item>
      </template>

      <v-divider></v-divider>

      <v-list density="compact" nav>
        <v-list-item
          prepend-icon="mdi-home-city"
          title="dashboard"
          value="dashboard"
        ></v-list-item>
        <v-list-item
          prepend-icon="mdi-account-group-outline"
          title="prelim"
          value="prelim"
          to="/prelim"
        ></v-list-item>
         <v-list-item
          prepend-icon="mdi-account-group-outline"
          title="calculate"
          value="calculate"
          to="/calculate"
        ></v-list-item>
        <v-list-item
          prepend-icon="mdi-account-group-outline"
          title="midterm"
          value="midterm"
          to="/midterm"
        ></v-list-item>
        

      </v-list>
    </v-navigation-drawer>

    <v-app-bar :elevation="2">
      <template v-slot:prepend>
        <v-app-bar-nav-icon @click="rail = !rail"></v-app-bar-nav-icon>
      </template>

      <v-app-bar-title>Application Bar</v-app-bar-title>
    </v-app-bar>
    <v-main>
      <v-container fluid>
        <slot />
      </v-container>
    </v-main> 
  </v-app>
</template>

<script  setup>
import { ref } from "vue";
const drawer = ref(true);
const rail = ref(true);
</script>

<style>
</style>
