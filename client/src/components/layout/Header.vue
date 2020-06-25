<template>
    <v-app-bar app color="blue-grey" dark>
        <v-app-bar-nav-icon @click="openDrawer"/>
        <router-link to="/" tag="button">DiscordServerTracker</router-link>
        <v-spacer/>
        <router-link to="/about" tag="button">About</router-link>
    </v-app-bar>
</template>

<script>
    import { EventBus } from "@/main";

    export default {
        name: "Header",
        methods: {
            openDrawer() {
                EventBus.$emit(('update:open'))
            }
        }
    }
</script>

<style scoped>

</style>