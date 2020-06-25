<template>
  <v-item-group light>
      <v-row rows="2">
        <v-col cols="3"
            v-for="item in servers" :key="item.id"
        >
          <v-item v-slot:default="{ active, toggle }">
            <v-card
                :color="active ? 'blue-grey' : ''"
                class="d-flex align-center"
                dark
                height="200"
                width="400"
                @click="toggle"
            >
              <div
                  v-if="active"
                  class="d-flex align-center text-center"
              >
                Server information
              </div>
              <div v-else
                   class="display-4 flex-grow-1 text-center">
                {{ item.title }}
              </div>
            </v-card>
          </v-item>
        </v-col>
      </v-row>
  </v-item-group>
</template>

<script>
export default {
  name: "ServerList",
  props: {
    servers: Array
  }
}
</script>

<style scoped>

</style>