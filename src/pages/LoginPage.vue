<template>
  <q-layout>
    <q-page-container>
      <q-page class="flex flex-center">
        <div>
          <q-card class="bg-black q-pa-md">
            <q-card-section>
              <h3 class="text-white">Let's get rocking!</h3>
            </q-card-section>
            <q-card-section>
              <q-input
                class="q-mt-md"
                v-model="user.email"
                type="email"
                bg-color="white"
                color="positive"
                label="Email"
                outlined
                lazy-rules
              />
              <q-input
                v-model="user.password"
                class="q-mt-md"
                :type="isPwd ? 'password' : 'text'"
                bg-color="white"
                color="positive"
                label="Password"
                outlined
                lazy-rules
              >
                <template v-slot:append>
                  <q-icon
                    :name="isPwd ? 'visibility_off' : 'visibility'"
                    class="cursor-pointer"
                    @click="isPwd = !isPwd"
                  />
                </template>
              </q-input>
            </q-card-section>
            <q-card-actions class="justify-center q-pa-md">
              <q-btn
                label="Register"
                color="positive"
                text-color="white"
                class="full-width text-weight-medium"
                @click="login"
              />
            </q-card-actions>
          </q-card>
          <div class="text-center q-mt-md">
            Don't have an account yet?
            <router-link to="/register" style="text-decoration: none;" class="text-primary text-weight-medium">
              Register
            </router-link>
          </div>
        </div>
      </q-page>
    </q-page-container>
  </q-layout>
</template>

<script setup>
  import { ref } from 'vue'
  import User from 'src/utils/models.js'

  const user = ref(User)
  const isPwd = ref(true)

  const login = () => {
    console.log(user.value)
  }
</script>