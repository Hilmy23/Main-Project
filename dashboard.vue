<template>
  <v-card class="mx-auto overflow-hidden" height="auto">
    <v-app-bar color="blue darken-2">
      <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>

      <v-col class="text-center"><strong>Aplikasi Kasir</strong></v-col>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" absolute temporary>
      
      <v-card class="mx-auto" width="300">
         <v-list>
      <v-list-item>
        <v-list-item-title>Pengaturan</v-list-item-title>
        <v-list-item-icon>
          <v-icon right>mdi-chevron-right</v-icon>
        </v-list-item-icon>
      </v-list-item>
      

      <v-list-group
        :value="true"
      >
        <template v-slot:activator>
          <v-list-item-title>Katalog</v-list-item-title>
        </template>

            <v-list-group no-action sub-group>
              <template v-slot:activator>
                  <v-list-item-title>Manajemen Stok</v-list-item-title>
              </template>
              <v-list-item-title v-text="title"></v-list-item-title>
              <v-list-item-icon>
                <v-icon v-text="icon"></v-icon>
              </v-list-item-icon>
            </v-list-group>

            <v-list-group no-action sub-group>
              <template v-slot:activator>
                <v-list-item-content>
                  <v-list-item-title>Riwayat Transaksi</v-list-item-title>
                </v-list-item-content>
              </template>
              <v-list-item-title v-text="title"></v-list-item-title>
              <v-list-item-icon>
                <v-icon v-text="icon"></v-icon>
              </v-list-item-icon>
            </v-list-group>
          </v-list-group>
        </v-list>

        <v-list-item>
          <v-list-item-title>Logout</v-list-item-title>
        <v-list-item-icon>
          <v-icon right>mdi-chevron-right</v-icon>
        </v-list-item-icon></v-list-item>
        <v-list-item> </v-list-item>
        <v-list-item> </v-list-item>
        <v-list-item> </v-list-item>
        <v-list-item> </v-list-item>
        <v-list-item> </v-list-item>
        <v-list-item> </v-list-item>
        <v-list-item> </v-list-item>
        <v-list-item> </v-list-item>
        <v-list-item> </v-list-item>
      </v-card>
    </v-navigation-drawer>

    <v-container class="d-flex justify-center"
      ><v-card width="95%" tile elevation="5" class="rounded-lg">
        <v-form>
          <v-card-text class="d-flex justify-space-between">
            <v-card tile elevation="1" class="ml-3 rounded-lg" width="45%">
              <v-text-field class="mr-3 ml-3" placeholder="Id Barang" />
            </v-card>
            <v-card tile elevation="1" class="mr-3 rounded-lg" width="45%">
              <v-text-field class="mr-3 ml-3" placeholder="Total Bayar (RP)"
            /></v-card>
          </v-card-text>
          <v-card-text class="d-flex justify-space-between">
            <v-card tile elevation="1" class="ml-3 rounded-lg" width="45%">
              <v-text-field class="mr-3 ml-3" placeholder="Nama Barang" />
            </v-card>
            <v-card tile elevation="1" class="mr-3 rounded-lg" width="45%">
              <v-text-field class="mr-3 ml-3" placeholder="Bayar (RP)"
            /></v-card>
          </v-card-text>
          <v-card-text class="d-flex justify-space-between">
            <v-card tile elevation="1" class="ml-3 rounded-lg" width="45%">
              <v-text-field class="mr-3 ml-3" placeholder="Harga (RP)" />
            </v-card>
            <v-card tile elevation="1" class="mr-3 rounded-lg" width="24%">
              <v-text-field class="mr-3 ml-3" placeholder="Kembali (RP)"
            /></v-card>
            <v-card-actions class="ml-5 mb-2">
              <v-btn color="#EC8322" width="95">Tambah</v-btn>
            </v-card-actions>
          </v-card-text>
          <v-card-text class="d-flex justify-space-between">
            <v-card tile elevation="1" class="ml-3 rounded-lg" width="45%">
              <v-text-field class="mr-3 ml-3" placeholder="Kuantitas" />
            </v-card>
          </v-card-text>
          <v-card-text class="d-flex justify-space-between">
            <v-card tile elevation="1" class="ml-3 rounded-lg" width="45%">
              <v-text-field class="mr-3 ml-3" placeholder="Sub total (RP)" />
            </v-card>
          </v-card-text>
          <v-card-text class="d-flex justify-space-between">
            <v-card tile elevation="1" class="ml-3 rounded-lg" width="45%">
              <v-text-field class="mr-3 ml-3" placeholder="Total PPN" />
            </v-card>
          </v-card-text>
        </v-form> </v-card
    ></v-container>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    drawer: false,
    group: null,
  }),
}
</script>
