<script setup>
import AppLayout from '@/components/layout/AppLayout.vue'
import RegisterForm from '@/components/auth/RegisterForm.vue'
</script>

<template>
  <AppLayout>
    <template #content
      ><v-row>
        <v-col cols="12" md="6" class="mx-auto pt-16">
          <v-card class="mx-auto" elevation="24">
            <template #title>
              <v-img
                class="mx-auto"
                src="/images/logo-favicon.jpg"
                :width="mobile ? '75%' : '25%'"
              ></v-img>
              <h3 class="font-weight-black text-center">Welcome to Cafézy</h3>
              <p class="text-center">Register</p>
            </template>

            <v-card-text class="bg-surface-light pt-4">
              <v-divider class="my-5"> </v-divider>

              <RegisterForm></RegisterForm>

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
