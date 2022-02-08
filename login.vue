<template>
  <v-app>
    <v-img :src="require('../assets/bg.png')" width="100%">
      <br />
       <v-card-title class="d-flex justify-center mt-16">
            <h1 class="font-weight-medium font-family-poppins">LOGIN</h1>
          </v-card-title>
      <v-container class="d-flex justify-center my-16">
          <v-form v-model="isvalid">
            <v-card tile elevation="5" class="mt-5 rounded-lg d-flex justify-center" width="400">
              <v-text-field
                class="ml-3 mr-3"
                :rules="emailRules"
                placeholder="Masukan Email Atau Username Anda"
                prepend-icon="mdi-account"
                v-model="user.email"
              />
            </v-card>
            <v-card tile elevation="5" class="mt-5 rounded-lg d-flex justify-center">
              <v-text-field
                class="ml-3 mr-3"
                :rules="passwordRules"
                placeholder="Masukan Password Anda"
                :type="showPassword ? 'text' : 'password'"
                :prepend-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'"
                @click:prepend="handleclick"
                v-model="user.password"
            /></v-card>

            <v-card-actions class="ml-2 mb-2 mt-4">
              <v-btn color="#008ac5" @click="handlesubmit"
                >Login</v-btn
              >
              <v-btn color="info">Register</v-btn>
            </v-card-actions>
          </v-form>
        
      </v-container>
    </v-img>
  </v-app>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      showPassword: false,
      user: {
        email: '',
        password: '',
      },
      emailRules: [(value) => value != '' || 'Email/Username is required'],
      passwordRules: [
        (value) => value != '' || 'Password is required',
        (value) => value.length <= 8 || 'Password maximal 8',
      ],
      isvalid: false,
    }
  },
  methods: {
    handleclick() {
      this.showPassword = !this.showPassword
    },
    handlesubmit() {
      console.log(this.user)
      this.user = {
        email: '',
        password: '',
      }
    },
  },
}
</script>