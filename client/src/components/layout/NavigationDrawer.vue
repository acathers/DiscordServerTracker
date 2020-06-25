<template>
    <v-navigation-drawer app class="drawer" v-model="open">
        <v-card>
            content
        </v-card>
    </v-navigation-drawer>
</template>

<script>
    import {EventBus} from "@/main";

    export default {
        name: "NavigationDrawer",
        data() {
            return {
                open: true
            }
        },
        methods: {
            drawer(){
                console.log(this.open);
                this.open = !this.open;
            }
        },
        mounted() {
            EventBus.$on('update:open', () => this.open = !this.open)
        }
    }
</script>

<style scoped>

</style>