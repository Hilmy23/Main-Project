<template>
  <v-app>
    <v-img :src="require('../assets/bg.png')" width="100%">
      <br />
      <br />
      <br />
      <v-icon class="d-flex justify-center mr-1" color="#616161" size="250"
        >mdi-message-processing</v-icon
      >
      <h2 class="d-flex justify-center" style="color: #008ac5">
        Verifikasi Diri Anda
      </h2>
      <p class="d-flex justify-center mt-2" style="color: black">
        Kami akan mengirimkan kode verifikasi
      </p>
      <p class="d-flex justify-center" style="color: black">
        Kepada anda pastikan email yang anda cantumkan telah sesuai
      </p>
      <v-container
        class="d-flex align-center justify-center"
        style="max-width: 250px"
      >
        <v-otp-input v-model="otp" type="number" length="4"></v-otp-input>
      </v-container>
      <v-card-actions class="d-flex justify-center">
        <p class="d-flex align-end mr-2" style="color: #2196f3">
          Tidak menerima email?
        </p>
        <v-btn color="white" style="color: black" class="mb-5" rounded-lg
          >kirim</v-btn
        >
      </v-card-actions>
    </v-img>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    otp: '',
  }),
}
</script>
