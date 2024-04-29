<template>
    <div class="container-fluid">
        <div class="row">
            <div class="col-lg 12">
                <h2 class="text-center my-4">ISI BUKU KUNJUNGAN</h2>
                <form>
                    <div class="mb-3">
                        <input type="text" class="form-control form control-lg rounded-5" placeholder="NAMA...">
                    </div>
                    <div class="mb-3">
                        <select class="form-control form-conntrol-lg form-select rounded-5">
                            <option value="">KATEGORI</option>
                            <option value="Siswa">Siswa</option>
                            <option value="Guru">Guru</option>
                            <option value="Staf">Staf</option>
                            <option value="Umum">Umum</option>
                        </select>
                    </div>
                    <div class="mb-3">
                        
                                <select class="form-control form-control-lg form-select rounded-5 mb-2">
                                    <option value="">KELAS</option>
                                    <option value="1">1</option>
                                    <option value="2">2</option>
                                    <option value="3">3</option>
                                    <option value="4">4</option>
                                </select>
                    </div>
                    <div class="mb-3">
                        <select class="form-control form-control-lg form-select rounded-5">
                            <option value="">KEPERLUAN</option>
                            <option value="baca">Baca Buku</option>
                            <option value="pinjam">Pinjam Buku</option>
                            <option value="kembalikan">Kembalikan Buku</option>
                        </select>
                    </div>
                    <button type="submit" class="btn btn-light btn-lg rounded-5 px-5">KIRIM</button>
                </form>
            </div>
        </div>
    </div>
</template>

<style scoped>
.form-control {
    background-color: #D9D9D9;
}

.btn{
    background-color: #D9D9D9;
}
</style>