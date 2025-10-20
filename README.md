# Laporan Praktikum 5: Javascript

1. Buatlah **_repository_** baru dengan nama **Lab5Web.**

2. Kerjakan semua latihan yang diberikan sesuai urutannya.

3. Screenshot setiap perubahannya.

4. Buatlah file **README.md** dan tuliskan penjelasan dari setiap langkah praktikum beserta screenshotnya.

5. **Commit** hasilnya pada **_repository_** masing-masing.

6. Kirim **URL _repository_** pada **_e-learning_** ecampus.

## Tugas

1. Buat script untuk melakukan validasi pada isian form.

  Program ini dibuat untuk mensimulasikan form pendaftaran workshop papercraft dengan validasi input menggunakan JavaScript.

    <!DOCTYPE html>
    <html lang="id">
    
    <head>
      <meta charset="UTF-8">
      <title>Form Pendaftaran Papercraft</title>
      <style>
        body { font-family: sans-serif; padding: 20px; }
        label { display: block; margin-top: 10px; }
      </style>
    </head>
    
    <body>
      <h2>Form Pendaftaran Workshop Papercraft</h2>
    
      <form onsubmit="return daftarPapercraft()">
        <label>Nama:
          <input type="text" id="nama">
        </label>
    
        <label>Umur:
          <input type="number" id="umur">
        </label>
    
        <label>Pilih jenis papercraft favorit:</label>
        <input type="checkbox" id="karakter" value="5000"> Karakter (Rp5000)<br>
        <input type="checkbox" id="hewan" value="7000"> Hewan (Rp7000)<br>
        <input type="checkbox" id="bangunan" value="10000"> Bangunan (Rp10000)<br>
    
        <label>Metode Pendaftaran:
          <select id="metode">
            <option value="online">Online</option>
            <option value="offline">Offline</option>
            <option value="cod">Bayar di tempat</option>
          </select>
        </label>
    
        <button type="submit">Daftar Sekarang</button>
      </form>
    
      <script>
        function daftarPapercraft() {
          let nama = document.getElementById("nama").value.trim();
          let umur = parseInt(document.getElementById("umur").value);
          let metode = document.getElementById("metode").value;
    
          // 1. Alert
          alert("Halo " + nama + "! Siap daftar papercraft?");
    
          // 2. Prompt
          let motivasi = prompt("Kenapa kamu suka papercraft?");
          if (motivasi) {
            alert("Motivasi kamu: " + motivasi);
          }
    
          // 3. Operasi Aritmatika
          let total = 0;
          if (document.getElementById("karakter").checked) total += 5000;
          if (document.getElementById("hewan").checked) total += 7000;
          if (document.getElementById("bangunan").checked) total += 10000;
    
          // 4. Seleksi if..else
          if (umur < 10) {
            alert("Kamu terlalu muda, tapi semangat kamu luar biasa!");
          } else if (umur > 60) {
            alert("Kamu legend! Papercraft cocok buat nostalgia.");
          } else {
            alert("Umur kamu pas banget buat jadi kreator papercraft.");
          }
    
          // 5. Switch
          switch (metode) {
            case "online":
              alert("Kamu memilih pendaftaran online. Praktis!");
              break;
            case "offline":
              alert("Kamu memilih datang langsung. Siap-siap bawa lem!");
              break;
            case "cod":
              alert("Bayar di tempat? Jangan lupa bawa uang pas.");
              break;
            default:
              alert("Metode tidak dikenali.");
          }
    
          // 7. Total harga otomatis
          alert("Total biaya papercraft kamu: Rp" + total);
    
          // 8. Keep it simple
          return false; // biar nggak reload halaman
        }
      </script>
    </body>
    </html>

## Hasil Web

  <img width="756" height="321" alt="image" src="https://github.com/user-attachments/assets/f364e446-d51a-46fc-b48c-ccc022267002" />

  <img width="755" height="306" alt="image" src="https://github.com/user-attachments/assets/d3996aea-e8f9-4645-9c22-e152c49568a7" />

  <img width="756" height="299" alt="image" src="https://github.com/user-attachments/assets/0176bba2-a399-486c-bcdd-f7a46e8ef28d" />

  <img width="758" height="318" alt="image" src="https://github.com/user-attachments/assets/6fad783a-a3ee-464f-998b-dc5309ca29ef" />

  <img width="760" height="319" alt="image" src="https://github.com/user-attachments/assets/fec8220f-46fb-4af1-957c-a53f0a15a954" />

  <img width="757" height="304" alt="image" src="https://github.com/user-attachments/assets/c52b0578-9f29-4d6c-8483-6e79a00dc77a" />

## Langkah-Langkah Praktikum

### Javascrip Dasar

1. Pemakaian Alert sebagai property window.

  **alert** digunakan untuk memberikan notifikasi langsung kepada pengguna, misalnya saat nama kosong atau umur tidak sesuai.

  <img width="959" height="264" alt="image" src="https://github.com/user-attachments/assets/f0cacb21-aa2b-4f3a-8313-9e8835763887" />

2.  Pemakaian method dalam objek.

  <img width="959" height="290" alt="image" src="https://github.com/user-attachments/assets/7e9ec388-a754-44b1-af7d-7bb657cfbce6" />

3. Pemakaian Prompt

  **prompt** digunakan untuk meminta input peserta secara interaktif.

  <img width="958" height="326" alt="image" src="https://github.com/user-attachments/assets/f76422b6-4b7d-4ebc-98b6-d89673dc7d9a" />

  <img width="958" height="312" alt="image" src="https://github.com/user-attachments/assets/cde8318a-a30a-46e6-90f3-e7051d22e887" />

4. Pembuatan fungsi dan cara pemanggilannya.

  <img width="959" height="232" alt="image" src="https://github.com/user-attachments/assets/2945419e-d8f6-4574-8f86-64010243e33f" />

### Dasar Pemrograman Di Javascript

1. Operasi dasar aritmatika

   Operasi aritmatika digunakan untuk menghitung total bilangan berdasarkan pilihan button.

              function test (val1,val2)
        {
          document.write("<br>"+"perkalian : val1*val2"+"<br>")
          document.write(val1*val2)
          document.write("<br>"+"pembagian : val1/val2"+"<br>")
          document.write(val1/val2)
          document.write("<br>"+"penjumlahan : val1+val2"+"<br>")
          document.write(val1+val2)
          document.write("<br>"+"pengurangan : val1*-val2"+"<br>")
          document.write(val1-val2)
          document.write("<br>"+"modulus : val1%val2"+"<br>")
          document.write(val1%val2)
        }

           <body onload=pesan()>
            <input type="button" name="button1" value="arithmetic" onclick=test(9,6)>
        </body>

  <img width="390" height="181" alt="image" src="https://github.com/user-attachments/assets/74635b08-7bfc-42c3-9209-10c020deec32" />

  <img width="390" height="244" alt="image" src="https://github.com/user-attachments/assets/bfff4b4d-74d4-48e7-a881-039505acbc0c" />

2. Seleksi kondisi (if..else)

   Struktur **if..else** digunakan untuk memberikan respon berdasarkan nilai Mahasiswa.

        <script languange="javascript">
            var nilai = prompt("Nilai (0-100): ", 0);
            var hasil = "";
            if (nilai >= 60)
            hasil = "lulus";
            else
            hasil = "tidak lulus"; 
            document.write ("hasil: " + hasil);
        </script>

  <img width="766" height="296" alt="image" src="https://github.com/user-attachments/assets/156ac11e-dc1e-4319-b187-a0df3ef0181c" />

  <img width="391" height="221" alt="image" src="https://github.com/user-attachments/assets/8518d9d3-dcae-4340-bc9c-247ee469b900" />

3. Penggunaan operator switch untuk seleksi kondisi

   Struktur **switch** digunakan untuk menampilkan pesan sesuai bilangan yang dipilih.

        <script languange="javascript">
                function test (){
                  val1=window.prompt("input nilai (1-5):")
                  switch (val1){
                    case "1" : document.write("Bilangan satu")
                        break
                    case "2" : document.write("Bilangan dua")
                        break
                    case "3" : document.write("Bilangan tiga")
                        break
                    case "4" : document.write("Bilangan empat")
                        break
                    case "5" : document.write("Bilangan lima")
                        break
                    default : document.write("Bilangan lainnya")
                  }
                }
            </script>

       <input type="button" name="button1" value="switch" onclick=test()>

  <img width="769" height="323" alt="image" src="https://github.com/user-attachments/assets/ce874c64-63b9-46a1-955d-94fb819b84aa" />

  <img width="390" height="184" alt="image" src="https://github.com/user-attachments/assets/114186da-56ae-44d5-8977-6d528e7c3b5b" />


### Pembuatan Form

1. Form Input

        <script languange="javascript">
            function test () {
                var val1=document.kirim.T1.value
                if (val1%2==0)
                    document.kirim.T2.value="Bilangan genap"
                else
                    document.kirim.T2.value="Bilangan ganjil"
            }
        </script>

           <form method="POST" name="kirim">
            <p>BIL <input type="text" name="T1" size="20">
            MERUPAKAN BIL <input type="text" name="T2" size="20"></p>
            <p><input type="button" value="TEBAK" name="B1" onclick=test()></p>
        </form>

  <img width="565" height="233" alt="image" src="https://github.com/user-attachments/assets/9b68fb26-b374-4da9-9d5d-bb4b27797382" />

2. Form Button

        <script languange="javascript">
            function ubahWarnaLB(warna) {
                document.bgColor = warna;
            }
            function ubahWarnaLD(warna) {
                document.fgColor = warna;
            }
        </script>

        <h1>Tes</h1>
        <form>
            <input type="button" value="Latar Belakang Hijau" onclick="ubahWarnaLB('GREEN')">
            <input type="button" value="Latar Belakang Putih" onclick="ubahWarnaLB('WHITE')">
            <input type="button" value="Teks Kuning" onclick="ubahWarnaLD('YELLOW')">
            <input type="button" value="Teks Biru" onclick="ubahWarnaLD('BLUE')">
        </form>
        <script languange="javascript">
            document.write("Dimodifikasi terakhir pada " + document.lastModified);
        </script>

  <img width="574" height="186" alt="image" src="https://github.com/user-attachments/assets/9a9f0fe2-e175-4272-a692-6386b04f3bfa" />

  <img width="562" height="213" alt="image" src="https://github.com/user-attachments/assets/5317be43-6953-4e96-bd47-452945e2cdd6" />

### HTML DOM

1. Pilihan menggunakan checkBox dengan perhitungan otomatis

        <script>
            function hitung(ele) {
                var total = document.getElementById('total').value;
                    total = (total ? parseInt(total) : 0);
                var harga = 0;
    
                if (ele.checked) {
                    harga = ele.value;
                    total += parseInt(harga);
                } else {
                    harga = ele.value;
                    if (total > 0)
                        total -= parseInt(harga);
                }
                document.getElementById('total').value = total;
            }
        </script>

        <h1>Daftar Menu Makanan</h1>
        <label><input type="checkbox" value="5000" id="menu1" onclick="hitung(this);" /> Ayam Goreng Rp. 5.000 </label><br/>
        <label><input type="checkbox" value="500" id="menu2" onclick="hitung(this);" /> Tempe Goreng Rp. 500 </label><br/>
        <label><input type="checkbox" value="2500" id="menu3" onclick="hitung(this);" /> Telur Dadar Rp. 2.500 </label><hr/>
        <strong>Total Bayar: Rp. <input id="total" type="text" /></strong>

  <img width="565" height="228" alt="image" src="https://github.com/user-attachments/assets/bfc2085f-a0d5-422a-b9e7-dae442f65f75" />

