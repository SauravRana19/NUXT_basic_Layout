<template>
    
    <v-layout>
        <ClientOnly>
            <Header @toggle="toggle = !toggle" />        
                <sidebar :toggle="toggle" />
                    <v-main class="d-flex align-center justify-center" >
                        <slot />
                     </v-main>
                 <v-footer name="footer" app>
                    <Footer />
                </v-footer>
        </ClientOnly>
    </v-layout>
</template>
<script setup lang="ts">
let toggle = ref(true)
</script>
<style></style>