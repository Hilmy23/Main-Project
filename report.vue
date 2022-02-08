<template>
  <v-timeline :dense="$vuetify.breakpoint.smAndDown">
    <v-timeline-item
      color="purple lighten-2"
      fill-dot
      right
    >
      <v-card>
        <v-card-title class="purple lighten-2">
          <v-icon
            dark
            size="42"
            class="mr-4"
          >
            mdi-magnify
          </v-icon>
          <h1 class="text-h4 white--text font-weight-light">
            Senin, 17 Januari 2022
          </h1>
        </v-card-title>
        <v-container>
          <v-row>
            <v-col
              cols="12"
              md="15"
              mt="mt-5"
            >
              Mempelajari Figma , Mempelajari GOIOT , Mempelajari fitur2 Workspace digoit
            </v-col>
            <v-col
              class="hidden-sm-and-down text-right"
              md="2"
            >
            </v-col>
          </v-row>
        </v-container>
      </v-card>
    </v-timeline-item>

    <v-timeline-item
      color="amber lighten-1"
      fill-dot
      left
      small
    >
      <v-card>
        <v-card-title class="amber lighten-1 justify-end">
          <h2 class="text-h4 mr-4 white--text font-weight-light">
            Selasa, 18 Januari 2022
          </h2>
          <v-icon
            dark
            size="42"
          >
            mdi-home-outline
          </v-icon>
        </v-card-title>
        <v-container>
          <v-row>
            <v-col
              cols="12"
              md="15"
            >
             Mencari Fitur2 epos yang ada, dan membuat laporan ttg epos
            </v-col>
            <v-col
              cols="12"
              md="4"
            >
            </v-col>
          </v-row>
        </v-container>
      </v-card>
    </v-timeline-item>

    <v-timeline-item
      color="cyan lighten-1"
      fill-dot
      right
    >
      <v-card>
        <v-card-title class="cyan lighten-1">
          <v-icon
            class="mr-4"
            dark
            size="42"
          >
            mdi-email-outline
          </v-icon>
          <h2 class="text-h4 white--text font-weight-light">
            Rabu, 19 Januari 2022
          </h2>
        </v-card-title>
        <v-container>
          <v-row>
            <v-col
              cols="12"
              md="15"
            >
             Menginstall NodeJs dan Mempelajari Vue.JS
            </v-col>
            <v-col
              cols="10"
              md="4"
            >
            </v-col>
          </v-row>
        </v-container>
      </v-card>
    </v-timeline-item>

    <v-timeline-item
      color="red lighten-1"
      fill-dot
      left
      small
    >
      <v-card>
        <v-card-title class="red lighten-1 justify-end">
          <h2 class="text-h4 mr-4 white--text font-weight-light">
            Kamis, 20 Januari 2022
          </h2>
          <v-icon
            dark
            size="42"
          >
            mdi-account-multiple-outline
          </v-icon>
        </v-card-title>
        <v-container>
          <v-row>
            <v-col
              cols="10"
              md="15"
            >
              Mempelajari Vue.JS dan Membuat Web Simple dengan Nuxt
            </v-col>
          </v-row>
        </v-container>
      </v-card>
    </v-timeline-item>

    <v-timeline-item
      color="green lighten-1"
      fill-dot
      right
    >
      <v-card>
        <v-card-title class="green lighten-1">
          <v-icon
            class="mr-4"
            dark
            size="42"
          >
            mdi-phone-in-talk
          </v-icon>
          <h2 class="text-h4 white--text font-weight-light">
            Jumat, 21 Januari 2022
          </h2>
        </v-card-title>
        <v-container>
          <v-row>
            <v-col>
              Membuat web sederhana sendiri menggunakan NUXT
            </v-col>
          </v-row>
        </v-container>
      </v-card>
    </v-timeline-item>
  </v-timeline>
</template>