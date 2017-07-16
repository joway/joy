<template>
  <v-app standalone>
    <v-navigation-drawer style="position: fixed" persistent v-model="drawer" class="pb-0" dark>
      <v-list>
        <v-list-tile class="mt-3">
          <v-list-tile-content>
            <v-list-tile-title>
              <span>Menu</span>
            </v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
        <v-divider></v-divider>
        <v-list-item>
          <v-list-tile>
            <v-list-tile-action>
              <v-icon dark>home</v-icon>
            </v-list-tile-action>
            <v-list-tile-content>
              <v-list-tile-title>Home</v-list-tile-title>
            </v-list-tile-content>
          </v-list-tile>
        </v-list-item>
        <v-list-item>
          <v-list-tile>
            <v-list-tile-action>
              <v-icon dark>home</v-icon>
            </v-list-tile-action>
            <v-list-tile-content>
              <v-list-tile-title>Home</v-list-tile-title>
            </v-list-tile-content>
          </v-list-tile>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  
    <v-toolbar class="indigo" style="position: fixed">
      <v-toolbar-title>
        <v-toolbar-side-icon dark @click.native.stop="drawer = !drawer"></v-toolbar-side-icon>
      </v-toolbar-title>
    </v-toolbar>
  
    <main class="main">
      <slot>
        只有在没有要分发的内容时才会显示。
      </slot>
    </main>
    <v-footer class="indigo" style="position: absolute;color: #fff;bottom: 0;width: 100%;">
      <span>© {{ new Date().getFullYear() }}</span>
    </v-footer>
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
