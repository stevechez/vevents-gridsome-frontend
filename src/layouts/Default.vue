<template>
  <v-app>
    <v-app-bar app>
      <v-toolbar-title>eVents</v-toolbar-title>

      <v-text-field
        placeholder="Placeholder"
        class="ml-8"
        style="max-width: 300px"
        prepend-inner-icon="mdi-magnify"
        outlined
        rounded
        dense
        hide-details
      />
      <v-spacer />
      <v-btn>Create Event</v-btn>
    </v-app-bar>
    <p>{{ $static.metadata.siteDescription }}</p>
    <v-main>
      <slot />
    </v-main>
  </v-app>
</template>

<static-query>
query {
  metadata {
    siteName
    siteDescription
  }
}
</static-query>

<style>
</style>
