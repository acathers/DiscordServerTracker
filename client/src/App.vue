<template>
    <v-app>
        <Header/>
        <NavigationDrawer/>
        <v-main>
            <v-container>
                <router-view/>
            </v-container>
        </v-main>
        <Footer/>
    </v-app>
</template>

<script>

    import Footer from "@/components/layout/Footer";
    import Header from "@/components/layout/Header";
    import NavigationDrawer from "@/components/layout/NavigationDrawer";
    export default {
        name: 'App',

        components: {NavigationDrawer, Header, Footer},

        data: () => ({
        }),
    };
</script>
