<template>
    <v-footer class="bg-teal ">
        <v-row justify="center" no-gutters>
            <div>
                <strong>Get connected with us on social networks!</strong>
                <v-spacer></v-spacer>

                <v-btn v-for="link in links" :key="link" :icon="link" class="mx-4" size="small" variant="plain"></v-btn>
            </div>
            <div>
                {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
            </div>
        </v-row>
    </v-footer>
</template>
<script setup lang="ts">
let links = reactive([
    'mdi-facebook',
    'mdi-twitter',
    'mdi-linkedin',
    'mdi-instagram',
])
</script>
<style scoped></style>