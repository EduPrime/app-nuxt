<script setup lang="ts">
const drawer = ref(true)
const rail = ref(true)
</script>

<template>
  <v-card>
    <v-layout>
      <v-navigation-drawer
        v-model="drawer"
        :rail="rail"
        permanent
        @click="rail = false"
      >
        <v-list-item
          id="eduprime-logo" prepend-avatar="~/assets/img/eduprime-logo.png"
          title="EduPrime"
          class="ml-2"
          nav
        >
          <template #append>
            <v-btn
              icon="mdi-chevron-left"
              variant="text"
              @click.stop="rail = !rail"
            />
          </template>
        </v-list-item>

        <v-divider />

        <v-list density="compact" nav>
          <v-list-item prepend-icon="mdi-home-city" title="Escola" value="Escola" href="/escola" />
          <v-list-item prepend-icon="mdi-account" title="My Account" value="account" />
          <v-list-item prepend-icon="mdi-account-group-outline" title="Users" value="users" />
        </v-list>
      </v-navigation-drawer>
      <v-main>
        <NuxtPage />
      </v-main>
    </v-layout>
  </v-card>
</template>
