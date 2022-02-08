<template>
  <div class="text-center">
    <v-dialog
      v-model="dialog"
      width="500"
    >
      <template v-slot:activator="{ on, attrs }">
        <v-btn
          color="teal darken-3"
          dark
          v-bind="attrs"
          v-on="on"
        >
          Klik Disini
        </v-btn>
      </template>

      <v-card>
        <v-card-title class="text-h5 indigo lighten-2">
          Ketentuan
        </v-card-title>

        <v-card-text class="mt-5">
           Registrasi Terlebih Dahulu
        </v-card-text>

        <v-divider></v-divider>

        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn
            color="primary"
            text
            @click="dialog = false"
          >
            I accept
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </div>
</template>
<script>
  export default {
    data () {
      return {
        dialog: false,
      }
    },
  }
</script>