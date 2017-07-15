<template>
  <v-app standalone>
    <v-navigation-drawer style="position: fixed" persistent absolute height="100%" clipped enable-resize-watcher v-model="drawer">
      <v-list dense>
        <v-subheader class="mt-3 grey--text text--darken-1">SUBSCRIPTIONS</v-subheader>
        <v-list-tile class="mt-3">
          <v-list-tile-action>
            <v-icon class="grey--text text--darken-1">add_circle_outline</v-icon>
          </v-list-tile-action>
          <v-list-tile-title class="grey--text text--darken-1">Browse Channels</v-list-tile-title>
        </v-list-tile>
        <v-list-tile>
          <v-list-tile-action>
            <v-icon class="grey--text text--darken-1">settings</v-icon>
          </v-list-tile-action>
          <v-list-tile-title class="grey--text text--darken-1">Manage Subscriptions</v-list-tile-title>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-toolbar class="blue" style="position: fixed">
      <v-toolbar-title>
        <v-toolbar-side-icon @click.native.stop="drawer = !drawer"></v-toolbar-side-icon>
      </v-toolbar-title>
    </v-toolbar>
    <main class="main">
      <v-container>
        <v-layout>
          <v-flex xs12>
            <slot>
              只有在没有要分发的内容时才会显示。
            </slot>
          </v-flex>
        </v-layout>
      </v-container>
    </main>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    drawer: true,
  }),
}
</script>

<style scoped>
.main {
  padding-top: 64px;
}
</style>
