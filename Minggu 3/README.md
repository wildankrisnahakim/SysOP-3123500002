<div align="center">
  <h1 style="font-weight: bold"> LAPORAN PRAKTIKUM III SISTEM OPERASI<br> Iops Dan Flops</h1>
  <h4 style="text-align: center;">Dosen Pengampu : Dr. Ferry Astika Saputra, S.T., M.Sc.</h4>
</div>
<br />
<br />
<div align="center">
  <img src="https://upload.wikimedia.org/wikipedia/id/4/44/Logo_PENS.png" alt="Logo PENS">
  <h3 style="text-align: center;">Disusun Oleh : </h3>
  <p style="tex-align: center;">
    Wildan Krisna Hakim (3123500002)<br>
    Firsty Angelica Valency (3123500029)<br>
    Hazel Mangadaralam Pratama Rayes (3123500024)<br>
  </p>
  <h3 style="text-align: center;line-height: 1.5">Program Studi Teknik Informatika<br>Departemen Teknik Informatika Dan Komputer<br>Politeknik Elektronika Negeri Surabaya<br>2023/2024</h3>
  <hr>
</div>
            
            
<h2 align="center"> Iops Dan Flops</h2>

<h3>Iops</h3>
<p>IOPS adalah jumlah permintaan yang dikirim aplikasi Anda ke disk penyimpanan dalam satu detik.</p>

<h3>Flops</h3>
<p>FLOPS adalah singkatan dari istilah dalam bahasa Inggris Floating point Operations Per Second yang merujuk pada satuan untuk jumlah perhitungan yang dapat dilakukan oleh sebuah perangkat komputasi (dalam hal ini adalah komputer) terhadap bilangan pecahan (floating point) tiap satu satuan waktu.</p>


<h2 align="center">Melakukan Benchmarking pada PC</h2>

1. **Melakukan Instalasi Package GCC,Make dan Git pada Debian 12 yang sudah terinstall**
<img src="img/sudoaptupdate.jpg" alt="">
<br>
<img src="img/sudogcc.jpg" alt="">

<p>Lakukan perintah "$ sudo apt update" pada terminal kemudian ketik "$ sudo apt install gcc" untuk menginstall compile dan "$ sudo apt install git" untuk menginstall git pada debian</p>


**2. Melakukan Git clone pada Debian 12**
<img src="img/gitclone.jpg" alt="">

<p>Arahkan direktori pada terminal yang ingin dituju lalu ketik "$ git clone (paste link github) lalu tekan enter</p>

**3. Melakukan Build Binaries,Cleaning, dan Install Binaries**
<img src="img/make.jpg" alt="">

<p>Arahkan direktori pada folder flops/iops yang telah dilakukan git clone pada langkah sebelumnya kemudian buka terminal dan ketik "$ make"</p>

<img src="img/makeclean.jpg" alt="">

<p>Kemudian lakukan perintah "$ make clean" lalu ketik "$ sudo make install" untuk menginstall binaries pada debian.</p>

**4. Melakukan Proses Benchmarking menggunakan Iops dan Flops**
<img src="img/iops64.jpg" alt="">

<p>Untuk benchmarking menggunakan iops ketik pada terminal "$ iops32 $(nproc)" atau iops64 sesuaikan dengan spesifikasi laptop yang dipakai</p>

<img src="img/flops64.jpg" alt="">

<p>Untuk benchmarking pada flops sama seperti iops hanya saja mengganti dari iops menjadi flops "$ flops32 $(nproc)" atau $ flops64 $(nproc)</p>


<h2 align="center">Analisa Hasil Benchmarking</h2>

<p justify-content="center">

|                      | IOPS64 (Integer)         | FLOPS64 (Floating Point)    |
|----------------------|------------------------|---------------------------|
| Total Throughput     | 13.857711 Gigaiops     | 13.727422 Gigaflops       |
| Single Core Throughput | 6.971539 Gigaiops   | 6.880348 Gigaflops       |
</p>

<p>Dengan melihat tabel di atas, dapat dilihat bahwa IOPS memiliki total throughput dan throughput single core yang lebih tinggi dibandingkan dengan FLOPS. Namun demikian, perbedaan antara total throughput dan throughput single core juga penting untuk diperhatikan karena menunjukkan seberapa baik CPU dapat mengalokasikan dan memanfaatkan sumber daya secara efisien antara inti tunggal dan total throughput.</p>

**REFERENSI** 

[MICROSOFT IOPS](https://learn.microsoft.com/id-id/azure/virtual-machines/premium-storage-performance)




















