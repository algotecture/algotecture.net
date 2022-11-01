<template>
  <v-app-bar
    app
    color="red accent-2"
  >
    <div class="d-flex align-center">
      <v-img
        alt="AgloTecture"
        class="shrink mr-2"
        contain
        src="@/assets/logo.png"
        transition="scale-transition"
        width="26"
      />
    <v-toolbar-title class="white--text">Algotecture</v-toolbar-title>
    </div>
    <v-spacer></v-spacer>
      <v-btn text ><router-link class="white--text" to="/">home</router-link> |</v-btn>
      <v-btn text ><router-link class="white--text" to="/ethics">ethics</router-link> |</v-btn>
      <v-btn text ><a class="white--text" href="">blog</a> |</v-btn>
      <v-btn text ><a class="white--text" href="https://github.com/algotecture/algotecture.net">code</a></v-btn>
  </v-app-bar>
</template>

<script>
export default {
  name: 'MenuNavigation',
  data: () => ({
  })
}
</script>
