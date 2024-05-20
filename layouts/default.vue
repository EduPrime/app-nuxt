<template>
  <v-layout class="rounded rounded-md">
    <v-app-bar
      color="surface-variant"
      title="Application bar"
    />

    <v-navigation-drawer>
      <v-list>
        <v-list-item title="Drawer left" />
      </v-list>
    </v-navigation-drawer>

    <v-navigation-drawer location="right">
      <v-list>
        <v-list-item title="Drawer right" />
      </v-list>
    </v-navigation-drawer>

    <v-main
      class="d-flex align-center justify-center"
      style="min-height: 300px"
    >
      <slot />
    </v-main>
  </v-layout>
</template>
