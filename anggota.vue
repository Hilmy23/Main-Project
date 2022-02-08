<template>
  <v-app>
      <v-simple-table
    fixed-header
    height="300px"
  >
    <template v-slot:default>
      <thead>
        <tr>
          <th class="text-left">
            Nama
          </th>
          <th class="text-left">
            Bagian
          </th>
          <th class="text-left">
            Nomer Telepon
          </th>
          <th class="text-left">
            Jenis Kelamin
          </th>
        </tr>
      </thead>
      <tbody>
        <tr
          v-for="item in datanya"
          :key="item.nama"
        >
          <td>{{ item.nama }}</td>
          <td>{{ item.bagian }}</td>
          <td>{{ item.nomertelpon }}</td>
          <td>{{ item.jk }}</td>
        </tr>
      </tbody>
    </template>
  </v-simple-table></v-app>
</template>
<script>
  export default {
    data () {
      return {
        datanya: [
          {
            nama: 'Muhammad Hilmy',
            bagian: 'Front-end',
            nomertelpon: '087871411983',
            jk: 'laki-laki',
          },
          {
            nama: 'Muhamad Iqbal',
            bagian: 'Front-end',
            nomertelpon: '0895704266850',
            jk: 'laki-laki',
          },
          {
            nama: 'Radia Hestianto',
            bagian: 'Back-end',
            nomertelpon: '0895349320142',
            jk: 'laki-laki',
          },
          {
            nama: 'Ziddan Azzahra',
            bagian: 'Back-end',
            nomertelpon: '089665316644',
            jk: 'laki-laki',
          },
          {
            nama: 'Zainul Ihsan',
            bagian: 'UI/UX',
            nomertelpon: '083890510438',
            jk: 'laki-laki',
          },
          {
          },
        ],
      }
    },
  }
</script>