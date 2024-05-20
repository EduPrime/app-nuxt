<script setup lang="ts">
const email = ref('')
const password = ref('')

function login() {
  // Aqui você pode adicionar a lógica de autenticação
  // console.log('Email:', email.value)
  // console.log('Password:', password.value)
}
</script>

<template>
  <v-container>
    <v-card>
      <v-card-title>Login</v-card-title>
      <v-card-text>
        <v-form @submit="login">
          <v-text-field
            v-model="email"
            label="Email"
          />
          <v-text-field
            v-model="password"
            label="Password"
            type="password"
          />
          <v-btn
            type="submit"
            color="primary"
          >
            Login
          </v-btn>
        </v-form>
      </v-card-text>
    </v-card>
  </v-container>
</template>
