<template>
    <v-navigation-drawer :clipped="true" app dark v-model="open">
        <v-card>

        </v-card>
    </v-navigation-drawer>
</template>

<script>
    import {EventBus} from "@/main";

    export default {
        name: "NavigationDrawer",
        data() {
            return {
              open
            }
        },
        methods: {
        },
        mounted() {
            EventBus.$on('update:open', () => this.open = !this.open);
        }
    }
</script>

<style scoped>
</style>