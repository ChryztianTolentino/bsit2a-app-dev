<template>
  <v-app>

     <!-- nav bar -->
    <v-navigation-drawer v-model="drawer"
      :rail="rail"
        permanent
        @click="rail = false"
      >
        <template v-slot:prepend>
          <v-list-item
            lines="two"
            subtitle="Logged in"
            title="Gerard Balasubas"
          ></v-list-item>
        </template>

        <v-divider></v-divider>

        <v-list density="compact" nav>
          <v-list-item prepend-icon="mdi-account" title="Dashboard" value="dashboard" to="/dashboard"></v-list-item>
          <v-list-item prepend-icon="mdi-home-city" title="Calculate" value="index" to="/calculate"></v-list-item>
          <v-list-item prepend-icon="mdi-account-group-outline" title="Prelim" value="prelim" to="/prelim"></v-list-item>
        </v-list>
      </v-navigation-drawer>

     <!-- app bar -->
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

      <!-- Script -->

<script setup>
const drawer = ref(true)
const rail = ref(true)
</script> 

<style>

</style>