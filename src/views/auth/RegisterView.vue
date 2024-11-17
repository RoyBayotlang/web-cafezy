<script setup>
import AppLayout from '@/components/layout/AppLayout.vue'
</script>

<template>
  <AppLayout>
    <template #content
      ><v-row>
        <v-col cols="12" md="6" class="mx-auto">
          <v-card class="mx-auto" elevation="24">
            <template #title>
              <h3 class="font-weight-black text-center">Welcome to Cafézy</h3>
              <p class="text-center">Register</p>
            </template>

            <v-card-text class="bg-surface-light pt-4">
              <v-divider class="my-5"> </v-divider>
              <v-form fast-fail @submit.prevent>
                <v-text-field label="FirstName" variant="outlined"></v-text-field>

                <v-text-field label="LastName" variant="outlined"></v-text-field>

                <v-text-field label="Email" variant="outlined"></v-text-field>

                <v-text-field label="Password" type="password" variant="outlined"></v-text-field>

                <v-text-field
                  label="Password Confirmation"
                  type="password"
                  variant="outlined"
                ></v-text-field>

                <v-btn
                  class="mt-2"
                  type="submit"
                  block
                  color="primary"
                  prepend-icon="mdi-account-plus"
                  >Register</v-btn
                >
              </v-form>
              <v-divider class="my-5"> </v-divider>

              <h5 class="text-center">
                Already Have Account? <RouterLink to="/">Click Here to Log-in</RouterLink>
              </h5>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row></template
    >
  </AppLayout>
</template>
