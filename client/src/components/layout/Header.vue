<template>
  <v-app-bar clipped-left app color="blue-grey" dark>
    <v-app-bar-nav-icon @click="openDrawer"/>
    <v-toolbar-title>
      <v-btn to="/">DiscordServerTracker</v-btn>
    </v-toolbar-title>
    <v-text-field
        v-model="searchInput"
        hide-details
        placeholder="Search"
        filled
        rounded
        dense
        single-line
        append-icon="fa-search" class="shrink mx-4"/>
    <v-spacer/>
    <router-link to="/about">About</router-link>
  </v-app-bar>
</template>

<script>
import {EventBus} from "@/main";

export default {
  name: "Header",
  data(){
    return {
      searchInput: ''
    }
  },
  methods: {
    openDrawer() {
      EventBus.$emit('update:open');
    }
  }
}
</script>

<style scoped>

</style>