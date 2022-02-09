<template>
  <v-card
    class="mx-auto overflow-hidden"
    height="657"
  >
    <v-app-bar
      color="#405A6A"
      dark
    >
      <v-app-bar-nav-icon @click="drawer = true"></v-app-bar-nav-icon>
         <v-card-actions>
         <v-btn color="#FF3333" 
          class="d-flex justify-end mb-6">logout</v-btn>
         </v-card-actions>
    </v-app-bar>

    <v-navigation-drawer
      v-model="drawer"
      absolute
      temporary 
    >
      <v-list
        nav
        dense
      >
        <v-list-item-group
          v-model="group"
          active-class="deep-purple--text text--accent-4"
          height
        >
          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-chevron-left</v-icon>
            </v-list-item-icon> 
          </v-list-item>

          <v-list-item>
            <v-list-item-icon class="mr-4">
              <v-icon>mdi-home</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Dashboard</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-calculator-variant</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Kasir Pintar</v-list-item-title>
          </v-list-item>

           <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-server 1</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Manajemen Stok</v-list-item-title>
          </v-list-item>

           <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-swap-horizontal 1</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Riwayat Transaksi</v-list-item-title>
          </v-list-item>

           <v-list-item>
            <v-list-item-icon>
              <v-icon>mdi-cog</v-icon>
            </v-list-item-icon>
            <v-list-item-title>Pengaturan</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
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