# Laporan Praktikum 5: Javascript

1. Buatlah **_repository_** baru dengan nama **Lab5Web.**

2. Kerjakan semua latihan yang diberikan sesuai urutannya.

3. Screenshot setiap perubahannya.

4. Buatlah file **README.md** dan tuliskan penjelasan dari setiap langkah praktikum beserta screenshotnya.

5. **Commit** hasilnya pada **_repository_** masing-masing.

6. Kirim **URL _repository_** pada **_e-learning_** ecampus.

## Tugas

1. Buat script untuk melakukan validasi pada isian form.

## Hasil Web



## Langkah-Langkah Praktikum

### Javascrip Dasar

1. Pemakaian Alert sebagai property window.

  <img width="959" height="264" alt="image" src="https://github.com/user-attachments/assets/f0cacb21-aa2b-4f3a-8313-9e8835763887" />

2.  Pemakaian method dalam objek.

  <img width="959" height="290" alt="image" src="https://github.com/user-attachments/assets/7e9ec388-a754-44b1-af7d-7bb657cfbce6" />

3. Pemakaian Prompt

  <img width="958" height="326" alt="image" src="https://github.com/user-attachments/assets/f76422b6-4b7d-4ebc-98b6-d89673dc7d9a" />

  <img width="958" height="312" alt="image" src="https://github.com/user-attachments/assets/cde8318a-a30a-46e6-90f3-e7051d22e887" />

4. Pembuatan fungsi dan cara pemanggilannya.

  <img width="959" height="232" alt="image" src="https://github.com/user-attachments/assets/2945419e-d8f6-4574-8f86-64010243e33f" />

### Dasar Pemrograman Di Javascript

1. Operasi dasar aritmatika

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


6. HTML DOM
