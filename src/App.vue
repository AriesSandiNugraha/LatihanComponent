<template>
  <Title title="Catatan Pengeluaran"/>
  <FormMahasiswa @entri-mahasiswa = "entriMahasiswa($event)"/>
  <ListMahasiswa v-if="dataMahasiswa.length>0" :dataMahasiswalist="dataMahasiswa"/>
  
</template>

<script>
import Title from './components/Title.vue'
import ListMahasiswa from './components/ListMahasiswa.vue'
import FormMahasiswa from './components/FormMahasiswa.vue'

export default {
  name: 'App',
  components: {
    Title,
    ListMahasiswa,
    FormMahasiswa,
  },
  data(){
    return {
      dataMahasiswa : [
        {nim : '111811006', nama : 'Aris', kelas : 'IF A'},
        {nim : '111811066', nama : 'Aries Sandi Nugraha', kelas : 'IF B'},
        {nim : '111811666', nama : 'Nugraha', kelas : 'IF C'}
      ],
    }
  },
  methods:{
    entriMahasiswa(event){
      this.dataMahasiswa.push(event);
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
