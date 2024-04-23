<template>
  <v-app-bar
    color="teal-darken-4"
    image="https://picsum.photos/1920/1080?random"
  >
    <template v-slot:image>
      <v-img
        gradient="to top right, rgba(19,84,122,.8), rgba(128,208,199,.8)"
      ></v-img>
    </template>

    <template v-slot:prepend>
      <v-app-bar-nav-icon @click="$emit('toggle')"></v-app-bar-nav-icon>
    </template>
    <v-app-bar-title>NUXT</v-app-bar-title>
    <v-spacer></v-spacer>
    <v-breadcrumbs :items="items">
      <template v-slot:divider>
        <h3>/</h3>
      </template>
    </v-breadcrumbs>

    <v-btn icon>
      <v-icon>mdi-magnify</v-icon>
    </v-btn>

    <v-btn :to="'/'" icon>
      <v-icon>mdi-home</v-icon>
    </v-btn>

    <v-btn icon>
      <v-icon>mdi-dots-vertical</v-icon>
    </v-btn>
  </v-app-bar>
</template>
<script setup lang="ts">

const emit = defineEmits(['toggle'])

let items = reactive([
  {
    title: "About",
    to: "about",
  },
  {
    title: "Contact",
    to: "contact",
  },
  {
    title: "Home",
    disabled: false,
    to: "Home",
  },
]);
</script>
