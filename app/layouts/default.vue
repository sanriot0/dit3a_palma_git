<template>
  <div>
    <v-app>
     <v-navigation-drawer
        v-model="drawer"
      >
        <v-list>
          <v-list-item
            prepend-avatar="https://i.pinimg.com/736x/70/47/f8/7047f8a9d9f8d4faf2d44b11a7d679b7.jpg"
            subtitle="DIT-3A"
            title="Sandra Palma"
          ></v-list-item>
        </v-list>

        <v-divider></v-divider>

        <v-list density="compact" nav>
          <v-list-item to="/" prepend-icon="mdi-monitor-dashboard" title="Dashboard" value="myfiles"></v-list-item>
          <v-list-item to="Inventory" prepend-icon="mdi-email-open-heart-outline" title="Inventory" value="shared"></v-list-item>
          <v-list-item to="Category" prepend-icon="mdi-star" title="Category" value="starred"></v-list-item>
          <v-list-item to="User" prepend-icon="mdi mdi-account" title="User" value="starred"></v-list-item>
        </v-list>
      </v-navigation-drawer>

      <v-app-bar :elevation="2">
  <template v-slot:prepend>
    <v-app-bar-nav-icon @click.stop="drawer =! drawer"></v-app-bar-nav-icon>
  </template>

  <v-app-bar-title>Application Bar</v-app-bar-title>
</v-app-bar>

    <v-main>
        <v-container>
            <slot/>
        </v-container>
    </v-main>

    </v-app>

  </div>
</template>

<script setup>
    const drawer=ref(true)
</script>
