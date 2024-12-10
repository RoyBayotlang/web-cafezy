<script setup>
import { requiredValidator, emailValidator } from '@/utils/validators'
import { ref } from 'vue'

const visible = ref(false)
</script>

<template>
  <v-form fast-fail @submit.prevent>
    <v-text-field
      label="Email"
      density="compact"
      variant="outlined"
      :rules="{ requiredValidator, emailValidator }"
    ></v-text-field>

    <v-text-field
      :append-inner-icon="visible ? 'mdi-eye-off' : 'mdi-eye'"
      :type="visible ? 'text' : 'password'"
      density="compact"
      placeholder="Enter your password"
      prepend-inner-icon="mdi-lock-outline"
      variant="outlined"
      @click:append-inner="visible = !visible"
      :rules="{ requiredValidator }"
    ></v-text-field>

    <v-btn class="mt-2" type="submit" block color="primary" prepend-icon="mdi-login">LogIn</v-btn>
  </v-form>
</template>
