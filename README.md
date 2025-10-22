# 🧾 Praktikum 5: JavaScript

### 👩‍💻 Identitas

**Nama:** Tiara Hayatul Khoir

**NIM:** 312410474

**Kelas:** TI.24.A.5

**Mata Kuliah:** Pemrograman Web

**Dosen Pengampu:** Agung Nugroho, S.Kom., M.Kom.

---

## 🎯 Tujuan Praktikum

1. Memahami sintaks dasar JavaScript.
2. Menggunakan JavaScript di dalam dokumen HTML.
3. Membuat kode JavaScript sederhana.
4. Melakukan manipulasi elemen HTML menggunakan JavaScript.

---

## ⚙️ Langkah-Langkah Praktikum

### 🔹 **Latihan 1 – Document Write & Console Log**

```html
<script>
    document.write("Hello World");
    console.log("Hello World");
</script>
```

**Penjelasan:**
Menampilkan teks “Hello World” di halaman web dan di console browser.

**Hasil:**
![Latihan 1](./screenshots/latihan1.png)

---

### 🔹 **Latihan 2 – Alert Box**

```html
<script>
    window.alert("ini merupakan pesan untuk anda!");
</script>
```

**Penjelasan:**
Menampilkan pesan pop-up menggunakan fungsi `window.alert()`.

**Hasil:**
![Latihan 2](./screenshots/latihan2.png)

---

### 🔹 **Latihan 3 – Script di Body**

```html
document.write("selamat mencoba javascript<br>");
document.write("semoga sukses!");
```

**Penjelasan:**
Menampilkan dua baris teks menggunakan `document.write()` di dalam `<body>`.

**Hasil:**
![Latihan 3](./screenshots/latihan3.png)

---

### 🔹 **Latihan 4 – Prompt Input**

```html
var nama = prompt("siapa nama anda?", "masukkan nama anda!");
document.write("hai, " + nama);
```

**Penjelasan:**
Mengambil input nama dari user menggunakan `prompt()` lalu menampilkannya.

**Hasil:**
![Latihan 4](./screenshots/latihan4.png)

---

### 🔹 **Latihan 5 – Body Onload**

```html
function pesan() {
    alert("memanggil javascript lewat body onload");
}
```

```html
<body onload="pesan()">
</body>
```

**Penjelasan:**
Fungsi `pesan()` dijalankan otomatis saat halaman selesai dimuat.

**Hasil:**
![Latihan 5](./screenshots/latihan5.png)

---

### 🔹 **Latihan 6 – Operasi Dasar Aritmatika**

```html
function test(val1, val2) {
    document.write("<br>perkalian : val1*val2<br>");
    document.write(val1 * val2);
    document.write("<br>pembagian : val1/val2<br>");
    document.write(val1 / val2);
    document.write("<br>penjumlahan : val1+val2<br>");
    document.write(val1 + val2);
    document.write("<br>pengurangan : val1-val2<br>");
    document.write(val1 - val2);
    document.write("<br>modulus : val1%val2<br>");
    document.write(val1 % val2);
}
```

**Penjelasan:**
Menampilkan hasil dari operasi aritmatika dasar (perkalian, pembagian, penjumlahan, pengurangan, dan modulus).

**Hasil:**
![Latihan 6](./screenshots/latihan6.png)

---

### 🔹 **Latihan 7 – Seleksi Kondisi If Else**

```html
var nilai = prompt("nilai (0-100): ", 0);
var hasil = "";
if (nilai >= 60)
    hasil = "lulus";
else
    hasil = "tidak lulus";
document.write("hasil: " + hasil);
```

**Penjelasan:**
Menentukan status kelulusan berdasarkan nilai input.

**Hasil:**
![Latihan 7](./screenshots/latihan7.png)

---

### 🔹 **Latihan 8 – Operator Switch**

```html
function test() {
    val1 = window.prompt("input nilai (1-5):")
    switch (val1) {
        case "1": document.write("bilangan satu"); break;
        case "2": document.write("bilangan dua"); break;
        case "3": document.write("bilangan tiga"); break;
        case "4": document.write("bilangan empat"); break;
        case "5": document.write("bilangan lima"); break;
        default: document.write("bilangan lainnya");
    }
}
```

**Penjelasan:**
Menggunakan `switch-case` untuk menampilkan teks sesuai angka yang dimasukkan user.

**Hasil:**
![Latihan 8](./screenshots/latihan8.png)

---

### 🔹 **Latihan 9 – Input Form dan Button**

```html
function test() {
    var val1 = document.kirim.T1.value;

    if (val1 % 2 == 0)
        document.kirim.T2.value = "bilangan genap";
    else
        document.kirim.T2.value = "bilangan ganjil";
}
```

**Penjelasan:**
User memasukkan bilangan ke form, lalu JavaScript menentukan apakah bilangan tersebut genap atau ganjil.

**Hasil:**
![Latihan 9](./screenshots/latihan9.png)

---

### 🔹 **Latihan 10 – HTML DOM**

```html
function hitungTotal() {
    var total = 0;
    if (document.getElementById("html").checked) total += 5000;
    if (document.getElementById("css").checked) total += 7000;
    if (document.getElementById("js").checked) total += 10000;

    document.getElementById("total").value = total;
}
```

**Penjelasan:**
Menggunakan HTML DOM untuk menghitung total harga otomatis berdasarkan checkbox yang dipilih user.

**Hasil:**
![Latihan 10](./screenshots/latihan10.png)

---

## 🧩 **Pertanyaan dan Tugas**

> Buat script untuk melakukan validasi pada isian form.

**Kode:**

```html
<html>
<head>
    <title>Validasi Form</title>
    <script language="javascript">
        function validasi() {
            var nama = document.formValidasi.nama.value;
            var email = document.formValidasi.email.value;
            var umur = document.formValidasi.umur.value;

            if (nama == "" || email == "" || umur == "") {
                alert("Semua field harus diisi!");
                return false;
            }

            if (email.indexOf("@") == -1 || email.indexOf(".") == -1) {
                alert("Alamat email tidak valid!");
                return false;
            }

            if (isNaN(umur)) {
                alert("Umur harus berupa angka!");
                return false;
            }

            alert("Form berhasil dikirim!");
            return true;
        }
    </script>
</head>

<body>
    <h2>Form Validasi</h2>
    <form name="formValidasi" onsubmit="return validasi()">
        Nama: <input type="text" name="nama"><br><br>
        Email: <input type="text" name="email"><br><br>
        Umur: <input type="text" name="umur"><br><br>
        <input type="submit" value="Kirim">
        <input type="reset" value="Reset">
    </form>
</body>
</html>
```

**Penjelasan:**

* Mengecek apakah seluruh field sudah diisi sebelum form dikirim.
* Memastikan email mengandung karakter `@` dan `.`.
* Mengecek bahwa umur hanya boleh angka.
* Jika valid, muncul pesan **“Form berhasil dikirim!”**.

**Hasil:**
![Validasi Form](./screenshots/validasi-form.png)

---

## 📚 **Kesimpulan**

Dari praktikum ini, saya memahami bahwa:

* JavaScript dapat digunakan untuk membuat halaman web lebih interaktif.
* Fungsi seperti `alert()`, `prompt()`, `document.write()`, `if-else`, dan `switch()` memungkinkan logika sederhana di browser.
* Melalui **HTML DOM**, JavaScript bisa berinteraksi langsung dengan elemen-elemen HTML.
* Validasi form membantu mencegah input kosong atau salah sebelum dikirim ke server.

---
