## 🧾 **README.md — Praktikum 5: JavaScript**

### 👩‍💻 Identitas

**Nama:** Tiara Hayatul Khoir
**NIM:** 312410474
**Kelas:** TI.24.A.5
**Mata Kuliah:** Pemrograman Web
**Dosen Pengampu:** Agung Nugroho, S.Kom., M.Kom.

---

## 🧠 **Tujuan Praktikum**

1. Mahasiswa mampu memahami sintaks dasar JavaScript.
2. Mahasiswa mampu menggunakan JavaScript pada dokumen HTML.
3. Mahasiswa mampu membuat kode JavaScript sederhana.
4. Mahasiswa mampu melakukan manipulasi elemen HTML menggunakan JavaScript.

---

## ⚙️ **Langkah-Langkah Praktikum**

### 🔹 **Latihan 1 – Document Write & Console Log**

Kode:

```html
<script>
    document.write("Hello World");
    console.log("Hello World");
</script>
```

**Penjelasan:**
Kode menampilkan teks “Hello World” di halaman web dan di console browser.
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
Script menampilkan pesan pop-up menggunakan fungsi `window.alert()`.
**Hasil:**
![Latihan 2](./screenshots/latihan2.png)

---

### 🔹 **Latihan 3 – Script di Body**

```html
document.write("selamat mencoba javascript<br>");
document.write("semoga sukses!");
```

**Penjelasan:**
Menampilkan dua baris teks menggunakan `document.write()` di dalam tag `<body>`.
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
Fungsi `pesan()` dipanggil otomatis saat halaman selesai dimuat.
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
Program menampilkan hasil operasi aritmatika sederhana (perkalian, pembagian, dst).
**Hasil:**
![Latihan 6](./screenshots/latihan6.png)

---

### 🔹 **Latihan 7 – Seleksi Kondisi If Else**

```html
var nilai = prompt("nilai (0-100): ", 0);
if (nilai >= 60)
    hasil = "lulus";
else
    hasil = "tidak lulus";
document.write("hasil: " + hasil);
```

**Penjelasan:**
Menentukan apakah user lulus atau tidak berdasarkan input nilai.
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
Menggunakan struktur `switch-case` untuk menampilkan teks sesuai input angka dari user.
**Hasil:**
![Latihan 8](./screenshots/latihan8.png)

---

### 🔹 **Latihan 9 – Pembuatan Form**

```html
<form name="formku">
  Nama: <input type="text" name="nama"><br>
  Umur: <input type="number" name="umur"><br>
  <input type="button" value="Tampilkan" onclick="tampilkanData()">
</form>
```

**Penjelasan:**
Membuat form sederhana dengan tombol yang memanggil fungsi JavaScript untuk menampilkan data yang diinputkan user.
**Hasil:**
![Latihan 9](./screenshots/latihan9.png)

---

### 🔹 **Latihan 10 – HTML DOM**

```html
function hitung() {
    var total = 0;
    if (document.getElementById("html").checked) total += 5000;
    if (document.getElementById("css").checked) total += 7000;
    if (document.getElementById("js").checked) total += 10000;
    document.getElementById("total").value = total;
}
```

**Penjelasan:**
Menggunakan HTML DOM untuk mengambil nilai checkbox dan menghitung total otomatis.
**Hasil:**
![Latihan 10](./screenshots/latihan10.png)

---

## 📸 **Kesimpulan**

Dari praktikum ini, saya memahami:

* JavaScript dapat disisipkan dalam HTML untuk mengatur interaksi halaman web.
* Fungsi seperti `alert()`, `prompt()`, `document.write()`, dan `switch()` digunakan untuk menampilkan serta memproses data.
* JavaScript juga mampu memanipulasi elemen HTML secara dinamis melalui **HTML DOM**.

---
