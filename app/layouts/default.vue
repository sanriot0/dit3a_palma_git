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
          <v-list-item prepend-icon="mdi-folder" title="My Files" value="myfiles"></v-list-item>
          <v-list-item prepend-icon="mdi-account-multiple" title="Shared with me" value="shared"></v-list-item>
          <v-list-item prepend-icon="mdi-star" title="Starred" value="starred"></v-list-item>
        </v-list>
      </v-navigation-drawer>

      <v-app-bar :elevation="2">
  <template v-slot:prepend>
    <v-app-bar-nav-icon @click.stop="drawer =! drawer"></v-app-bar-nav-icon>
  </template>

  <v-app-bar-title>Application Bar</v-app-bar-title>
</v-app-bar>

    <v-mian>
        <v-container>
            <slot/>
        </v-container>
    </v-mian>

    </v-app>

  </div>
</template>

<script setup>
    const drawer=ref(true)
</script>
