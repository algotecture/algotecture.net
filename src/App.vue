<template>
  <v-app>
    <menu-navigation />
    <v-main>
      <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script>
import MenuNavigation from '@/components/MenuNavigation'

export default {
  name: 'App',
  components: {
    MenuNavigation
  },
  data: () => ({
    //
  })
}
</script>
