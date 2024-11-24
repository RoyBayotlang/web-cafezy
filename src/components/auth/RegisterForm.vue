<template>
  <v-form fast-fail @submit.prevent>
    <v-text-field label="FirstName" density="compact" variant="outlined"></v-text-field>

    <v-text-field label="LastName" density="compact" variant="outlined"></v-text-field>

    <v-text-field label="Email" density="compact" variant="outlined"></v-text-field>

    <v-text-field
      :append-inner-icon="visible ? 'mdi-eye-off' : 'mdi-eye'"
      :type="visible ? 'text' : 'password'"
      density="compact"
      placeholder="Enter your password"
      prepend-inner-icon="mdi-lock-outline"
      variant="outlined"
      @click:append-inner="visible = !visible"
    ></v-text-field>

    <v-text-field
      :append-inner-icon="visible ? 'mdi-eye-off' : 'mdi-eye'"
      :type="visible ? 'text' : 'password'"
      density="compact"
      placeholder="Confirm your password"
      prepend-inner-icon="mdi-lock-outline"
      variant="outlined"
      @click:append-inner="visible = !visible"
    ></v-text-field>

    <v-btn class="mt-2" type="submit" block color="primary" prepend-icon="mdi-account-plus"
      >Register</v-btn
    >
  </v-form>
</template>
