<template>
  <v-app>
    <v-app-bar flat dense :absolute="!fixed" app color="#FFFFFF">
      <v-spacer></v-spacer>

      <v-btn icon href="https://github.com/isrc-cas/tarsier-meta/blob/main/roadmap/checklist.md">
        <v-icon>mdi-github</v-icon>
      </v-btn>

    </v-app-bar>
    <v-main>
      <v-container fluid>
        <router-view></router-view>
      </v-container>
    </v-main>

    <v-footer :absolute="!fixed" app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {
    }
  },
  methods: {
    handle(url)
    {
      window.location.href = url
    }
  }
}
</script>
