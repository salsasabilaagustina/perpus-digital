<template>
    <div class="container-fluid">
        <div class="row">
            <div class="col-lg-12">
                <h2 class="text-center my-4">RIWAYAT KUNJUNGAN</h2>
                <div class="my-3">
                    <input type="search" class="form-control form-control-lg rounded-5" placeholder="Filter...">
                </div>
                <div class="my-3 text-muted">menampilkan 3 dari 3</div>
                <table class="table">
                    <thead>
                        <tr>
                            <td>#</td>
                            <td>NAMA</td>
                            <td>KEANGGOTAAN</td>
                            <td>WAKTU</td>
                            <td>KEPERLUAN</td>
                        </tr>
                    </thead>
                    <tbody>
                        <tr v-for="(visitor,i) in visitors" :key="i">
                            <td>{{  i+1 }}.</td>
                            <td>{{  visitor.nama }}.</td>
                            <td>{{  visitor.keanggotaan?.nama }}.</td>
                            <td>{{  visitor.tanggal }},{{ visitor.waktu }}</td> 
                            <td>{{  visitor.keperluan?.nama }}.</td>
                        </tr>
                    </tbody>
                </table>
                <nuxt-link to="/pengunjung/tambah">
                    <button type="submit" class="btn btn-light btn-lg rounded-5 px-5">KEMBALI</button>
                </nuxt-link>
            </div>
        </div>
    </div>
</template>

<script setup>
const supabase= useSupabaseClient()

const visitors = ref([])

const getpengunjung = async () => {
    const {data,  error} = await supabase.from('pengunjung').select('*, keanggotaan(*), keperluan(*)')
    if(data) visitors.value = data
}

onMounted(() => {
    getpengunjung()
})
</script>

<style scoped>
.form-control{
    background-color: #D9D9D9;
}
.btn{
    background-color: #D9D9D9;
}
</style>