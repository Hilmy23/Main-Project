<template>
  <v-app>
     <v-img :src="require('../assets/bg.png')" width="100%">
      <h1 class="d-flex justify-center">REGISTRASI</h1>
    <v-container class="d-flex justify-center">
      <v-card width="90%" height="525" tile elevation="1" >

    <v-form v-model="isvalid">
      <v-card-text>
          <v-text-field class="ml-3 mr-3" :rules="namaRules" label="Nama" v-model="user.Nama"/>   
          <v-text-field class="ml-3 mr-3" :rules="nomerteleponRules" label="Nomer Telepon" v-model="user.Nomertelpon"/>
          <v-text-field class="ml-3 mr-3" :rules="emailRules" label="Email"  v-model="user.email"/>
          <v-text-field class="ml-3 mr-3" :rules="passwordRules" label="Password" 
            :type="showPassword ? 'text' : 'password'" 
            :append-icon="showPassword ? 'mdi-eye' : 'mdi-eye-off'" 
            @click:append="handleclick" v-model="user.password"/>
          <v-text-field class="ml-3 mr-3" :rules="namatokoRules" label="Nama Toko" v-model="user.NamaToko"/>
          <v-text-field class="ml-3 mr-3" :rules="jenisusahaRules" label="Jenis Usaha" v-model="user.JenisUsaha"/>
      </v-card-text>

      <v-card-actions class="d-flex justify-center ">
        <v-btn color="#005AC5" @click="handlesubmit" :disabled="!isvalid" width="98%">LANJUTKAN</v-btn>
      </v-card-actions>
      </v-form> 
    </v-card>
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
      user:{
        Nama:'',
        NomerTelepon:'',
        email:'',
        password:'',
        NamaToko:'',
        JenisUsaha:''
      },
       namaRules: [
        v => v !=''||'Isi Nama Terlebih Dahulu'
      ],
      nomerteleponRules: [
        v => v !=''||'Isi Nomer Telepon Terlebih Dahulu'
      ],
      emailRules: [
        v => v !=''||'Email Terlebih dahulu'
      ],
      passwordRules: [
        v => v !=''||'Isi Password Terlebih dahulu',
        v => v.length <= 8 || 'Password Max 8 Karakter'
      ],
       namatokoRules: [
        v => v !=''||'Isi Nama Toko Terlebih Dahulu'
      ],
       jenisusahaRules: [
        v => v !=''||'Isi Jenis Usaha Terlebih Dahulu'
      ],
      isvalid: false
    }
  },
  methods: {
    handleclick() {
      this.showPassword = !this.showPassword
    },
    handlesubmit(){
      console.log(this.user)
      this.user= {
        Nama:'',
        NomerTelepon:'',
        email: '',
        password: '',
        NamaToko:'',
        JenisUsaha:''
      }
    }
  }
};
</script>