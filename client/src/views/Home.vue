<template>
  <div>
    <ServerList :servers='servers'/>
  </div>
</template>

<script>

import ServerList from "@/components/ServerList";

export default {
  name: 'Home',
  components: {ServerList},
  data() {
    return {
      servers: [
        {
          id: 1,
          title: 'test1'
        },
        {
          id: 2,
          title: 'test2'
        },
        {
          id: 3,
          title: 'test1'
        },
        {
          id: 4,
          title: 'test2'
        },
        {
          id: 5,
          title: 'test1'
        },
        {
          id: 6,
          title: 'test2'
        }
      ]
    }
  }
}
</script>
