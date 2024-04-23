<template>
  <ClientOnly>
        <v-navigation-drawer v-model="props.toggle" expand-on-hover  rail >
          <v-list-item prepend-avatar="https://randomuser.me/api/portraits/men/85.jpg" title="John Leider" nav>
           
          </v-list-item>

          <v-divider></v-divider>

          <v-list density="compact" nav>
            <v-list-item prepend-icon="mdi-home-city" title="Home" value="home"></v-list-item>
            <v-list-item prepend-icon="mdi-account" title="My Account" value="account"></v-list-item>
            <v-list-item prepend-icon="mdi-account-group-outline" title="Users" value="users"></v-list-item>
          </v-list>
        </v-navigation-drawer>
  </ClientOnly>

</template>
<script setup lang="ts">
let props = defineProps({
  toggle: { type: Boolean, },
})
</script>