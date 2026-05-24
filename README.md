# Website Profil Siswa

Website ini adalah project sederhana untuk tugas sekolah SMK.  
Website dibuat menggunakan **HTML, CSS, dan JavaScript** dalam satu file utama yaitu `index.html`.

Website ini memiliki fitur:

1. Halaman login
2. Halaman profil siswa dan sekolah
3. Form edit profil
4. Fitur ubah password
5. Logout
6. Penyimpanan data menggunakan `localStorage`
7. Dapat diakses secara online menggunakan GitHub Pages

---

## Link Website

Website dapat diakses melalui:

```text
https://ayranathasya2009.github.io/website-profil-siswa/
```

---

## Tujuan Pembuatan Website

Tujuan dari website ini adalah untuk belajar dasar-dasar pembuatan website, yaitu:

- Mengenal struktur dasar HTML
- Mengenal penggunaan CSS untuk tampilan
- Mengenal JavaScript untuk membuat website menjadi interaktif
- Mengenal form input
- Mengenal sistem login sederhana
- Mengenal penyimpanan data tanpa database menggunakan `localStorage`
- Mengenal cara upload website ke GitHub Pages

---

## Teknologi yang Digunakan

Website ini menggunakan tiga teknologi dasar web:

| Teknologi | Fungsi |
|---|---|
| HTML | Membuat struktur halaman website |
| CSS | Mengatur tampilan website agar lebih menarik |
| JavaScript | Membuat fungsi login, edit profil, ubah password, dan logout |
| localStorage | Menyimpan data di browser tanpa database |
| GitHub Pages | Menampilkan website secara online |

---

## Struktur File

Project ini hanya menggunakan satu file utama:

```text
website-profil-siswa/
└── index.html
```

Penjelasan:

- `index.html` adalah file utama website.
- Di dalam file ini terdapat kode HTML, CSS, dan JavaScript.
- Karena masih sederhana, semua kode digabung dalam satu file agar mudah dipahami.

---

## Akun Login Default

Akun login awal yang digunakan adalah:

```text
Username: admin
Password: 1234567@888
```

Username masih dibuat tetap, yaitu `admin`.

Password dapat diubah melalui menu **Ubah Password** setelah berhasil login.

---

## Alur Penggunaan Website

Alur penggunaan website adalah sebagai berikut:

```text
Buka Website
     ↓
Halaman Login
     ↓
Masukkan Username dan Password
     ↓
Jika benar, masuk ke halaman utama
     ↓
Melihat profil siswa dan sekolah
     ↓
Bisa mengedit profil
     ↓
Bisa mengubah password
     ↓
Logout
```

---

## Cara Menjalankan Website di Laptop

Jika ingin menjalankan website secara lokal di laptop:

1. Download atau clone project dari GitHub.
2. Buka folder project.
3. Klik dua kali file:

```text
index.html
```

4. Website akan terbuka di browser.
5. Login menggunakan username dan password default.

---

## Cara Menjalankan Website Online

Website ini sudah di-upload ke GitHub dan dijalankan menggunakan GitHub Pages.

Langkah umum yang dilakukan:

1. Membuat akun GitHub.
2. Membuat repository baru.
3. Upload file `index.html`.
4. Masuk ke menu **Settings**.
5. Pilih menu **Pages**.
6. Pilih source dari branch `main`.
7. Simpan pengaturan.
8. GitHub akan membuat link website secara otomatis.

---

# Penjelasan Kode

Di dalam file `index.html`, terdapat tiga bagian utama:

1. HTML
2. CSS
3. JavaScript

---

## 1. Penjelasan Bagian HTML

HTML digunakan untuk membuat struktur halaman website.

Contoh struktur awal:

```html
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <title>Website Profil Siswa</title>
</head>
<body>
</body>
</html>
```

Penjelasan:

| Kode | Penjelasan |
|---|---|
| `<!DOCTYPE html>` | Menandakan bahwa dokumen ini adalah HTML5 |
| `<html lang="id">` | Menandakan bahwa bahasa halaman adalah Bahasa Indonesia |
| `<head>` | Berisi informasi website seperti judul dan pengaturan tampilan |
| `<body>` | Berisi isi utama yang tampil di browser |
| `<title>` | Judul halaman yang muncul di tab browser |

---

## 2. Penjelasan Bagian Login

Bagian login digunakan agar pengguna harus memasukkan username dan password sebelum melihat profil.

Contoh kode:

```html
<div id="loginPage" class="card">
  <h2>Login</h2>

  <label>Username</label>
  <input type="text" id="username" placeholder="Masukkan username">

  <label>Password</label>
  <input type="password" id="password" placeholder="Masukkan password">

  <button onclick="login()">Login</button>
</div>
```

Penjelasan:

| Kode | Fungsi |
|---|---|
| `id="loginPage"` | Menandai bagian halaman login |
| `<input type="text">` | Input untuk username |
| `<input type="password">` | Input untuk password |
| `placeholder` | Teks petunjuk di dalam input |
| `<button>` | Tombol untuk login |
| `onclick="login()"` | Saat tombol diklik, menjalankan fungsi `login()` |

---

## 3. Penjelasan Halaman Utama

Setelah login berhasil, pengguna masuk ke halaman utama.

Di halaman utama terdapat beberapa tombol:

```html
<button onclick="showSection('profileSection')">Profil</button>
<button onclick="showSection('editSection')">Edit Profil</button>
<button onclick="showSection('passwordSection')">Ubah Password</button>
<button onclick="logout()">Logout</button>
```

Penjelasan:

| Tombol | Fungsi |
|---|---|
| Profil | Menampilkan data profil siswa dan sekolah |
| Edit Profil | Membuka form untuk mengubah data profil |
| Ubah Password | Membuka form untuk mengganti password |
| Logout | Keluar dari halaman utama dan kembali ke login |

---

## 4. Penjelasan Bagian Profil

Bagian profil digunakan untuk menampilkan data siswa dan sekolah.

Contoh kode:

```html
<p><b>Nama:</b> <span id="viewNama"></span></p>
<p><b>Kelas:</b> <span id="viewKelas"></span></p>
<p><b>Jurusan:</b> <span id="viewJurusan"></span></p>
```

Penjelasan:

| Kode | Fungsi |
|---|---|
| `<p>` | Membuat paragraf |
| `<b>` | Membuat teks menjadi tebal |
| `<span>` | Tempat menampilkan data |
| `id="viewNama"` | Tempat untuk menampilkan nama siswa |
| `id="viewKelas"` | Tempat untuk menampilkan kelas |
| `id="viewJurusan"` | Tempat untuk menampilkan jurusan |

Data pada bagian ini diisi menggunakan JavaScript.

---

## 5. Penjelasan Form Edit Profil

Form edit profil digunakan untuk mengubah data siswa dan sekolah.

Contoh kode:

```html
<label>Nama Siswa</label>
<input type="text" id="nama">

<label>Kelas</label>
<input type="text" id="kelas">

<label>Jurusan</label>
<input type="text" id="jurusan">
```

Penjelasan:

| Kode | Fungsi |
|---|---|
| `<label>` | Memberi keterangan pada input |
| `<input>` | Tempat mengetik data |
| `id="nama"` | Input untuk nama siswa |
| `id="kelas"` | Input untuk kelas |
| `id="jurusan"` | Input untuk jurusan |

Setelah data diisi, pengguna menekan tombol:

```html
<button onclick="saveProfile()">Simpan Profil</button>
```

Tombol tersebut menjalankan fungsi `saveProfile()` untuk menyimpan data.

---

## 6. Penjelasan Form Ubah Password

Form ubah password digunakan untuk mengganti password login.

Contoh kode:

```html
<label>Password Lama</label>
<input type="password" id="oldPassword">

<label>Password Baru</label>
<input type="password" id="newPassword">

<label>Ulangi Password Baru</label>
<input type="password" id="confirmPassword">
```

Penjelasan:

| Input | Fungsi |
|---|---|
| `oldPassword` | Untuk mengetik password lama |
| `newPassword` | Untuk mengetik password baru |
| `confirmPassword` | Untuk mengulangi password baru |

Password baru hanya akan disimpan jika:

1. Password lama benar
2. Password baru minimal 4 karakter
3. Password baru dan konfirmasi password sama

---

# Penjelasan CSS

CSS digunakan untuk mengatur tampilan website.

---

## 1. Mengatur Semua Elemen

```css
* {
  box-sizing: border-box;
  font-family: Arial, sans-serif;
}
```

Penjelasan:

| Kode | Fungsi |
|---|---|
| `*` | Berlaku untuk semua elemen |
| `box-sizing: border-box` | Membuat ukuran elemen lebih mudah diatur |
| `font-family` | Mengatur jenis huruf |

---

## 2. Mengatur Body

```css
body {
  margin: 0;
  background: #eef3f8;
  color: #333;
}
```

Penjelasan:

| Kode | Fungsi |
|---|---|
| `margin: 0` | Menghapus jarak bawaan browser |
| `background` | Mengatur warna latar belakang |
| `color` | Mengatur warna teks |

---

## 3. Mengatur Card

```css
.card {
  background: #fff;
  padding: 25px;
  border-radius: 12px;
  box-shadow: 0 5px 15px rgba(0,0,0,0.1);
}
```

Penjelasan:

| Kode | Fungsi |
|---|---|
| `background: #fff` | Membuat warna kotak menjadi putih |
| `padding: 25px` | Memberi jarak di dalam kotak |
| `border-radius: 12px` | Membuat sudut kotak melengkung |
| `box-shadow` | Memberi efek bayangan |

---

## 4. Mengatur Tombol

```css
button {
  padding: 10px 16px;
  border: none;
  border-radius: 8px;
  background: #1e88e5;
  color: white;
  cursor: pointer;
}
```

Penjelasan:

| Kode | Fungsi |
|---|---|
| `padding` | Mengatur ukuran tombol |
| `border: none` | Menghilangkan garis tepi tombol |
| `border-radius` | Membuat tombol melengkung |
| `background` | Mengatur warna tombol |
| `color: white` | Mengatur warna tulisan tombol |
| `cursor: pointer` | Mengubah kursor menjadi tangan saat diarahkan ke tombol |

---

## 5. Class Hidden

```css
.hidden {
  display: none;
}
```

Penjelasan:

Class `hidden` digunakan untuk menyembunyikan bagian halaman.

Contohnya:

```html
<div id="mainPage" class="hidden">
```

Artinya halaman utama disembunyikan terlebih dahulu sebelum login berhasil.

---

## 6. Responsive Design

```css
@media (max-width: 600px) {
  .profile-box {
    grid-template-columns: 1fr;
  }
}
```

Penjelasan:

Kode ini membuat tampilan website tetap rapi saat dibuka di layar kecil seperti handphone.

Jika ukuran layar kurang dari 600px, maka tampilan profil yang awalnya dua kolom akan berubah menjadi satu kolom.

---

# Penjelasan JavaScript

JavaScript digunakan untuk membuat website bisa berfungsi, seperti login, logout, edit profil, dan ubah password.

---

## 1. Username dan Password Default

```javascript
const defaultUsername = "admin";
const defaultPassword = "1234567@888";
```

Penjelasan:

| Kode | Fungsi |
|---|---|
| `const` | Membuat variabel yang nilainya tetap |
| `defaultUsername` | Menyimpan username awal |
| `defaultPassword` | Menyimpan password awal |

---

## 2. Menyimpan Password Awal

```javascript
if (!localStorage.getItem("loginPassword")) {
  localStorage.setItem("loginPassword", defaultPassword);
}
```

Penjelasan:

Kode ini mengecek apakah password sudah tersimpan di browser.

Jika belum ada, maka password default akan disimpan ke `localStorage`.

Alurnya:

```text
Cek apakah loginPassword sudah ada
     ↓
Jika belum ada
     ↓
Simpan defaultPassword ke localStorage
```

---

## 3. Menyimpan Data Profil Awal

```javascript
if (!localStorage.getItem("profileData")) {
  const defaultProfile = {
    nama: "Nama Siswa",
    kelas: "X Animasi B",
    jurusan: "Animasi",
    alamat: "Cimahi, Jawa Barat",
    sekolah: "SMK Negeri 2 Cimahi",
    alamatSekolah: "Alamat sekolah",
    website: "https://smkn2cmi.sch.id/"
  };

  localStorage.setItem("profileData", JSON.stringify(defaultProfile));
}
```

Penjelasan:

Kode ini digunakan untuk membuat data profil awal.

Data tersebut berisi:

- Nama siswa
- Kelas
- Jurusan
- Alamat
- Nama sekolah
- Alamat sekolah
- Website sekolah

Karena `localStorage` hanya menyimpan teks, maka object JavaScript harus diubah menjadi teks menggunakan:

```javascript
JSON.stringify(defaultProfile)
```

---

## 4. Fungsi Login

```javascript
function login() {
  const username = document.getElementById("username").value;
  const password = document.getElementById("password").value;
  const savedPassword = localStorage.getItem("loginPassword");

  if (username === defaultUsername && password === savedPassword) {
    localStorage.setItem("isLogin", "true");
    showMainPage();
  } else {
    showMessage("loginMessage", "Username atau password salah!", "error");
  }
}
```

Penjelasan:

Fungsi ini berjalan saat tombol login diklik.

Langkah kerjanya:

1. Mengambil username yang diketik.
2. Mengambil password yang diketik.
3. Mengambil password yang tersimpan di browser.
4. Mengecek apakah username dan password benar.
5. Jika benar, masuk ke halaman utama.
6. Jika salah, tampilkan pesan error.

Bagian penting:

```javascript
document.getElementById("username").value
```

Artinya mengambil isi input dengan id `username`.

---

## 5. Fungsi Logout

```javascript
function logout() {
  localStorage.removeItem("isLogin");
  document.getElementById("mainPage").classList.add("hidden");
  document.getElementById("loginPage").classList.remove("hidden");
}
```

Penjelasan:

Fungsi ini digunakan untuk keluar dari halaman utama.

Saat logout:

1. Data status login dihapus.
2. Halaman utama disembunyikan.
3. Halaman login ditampilkan kembali.

---

## 6. Fungsi Menampilkan Halaman Utama

```javascript
function showMainPage() {
  document.getElementById("loginPage").classList.add("hidden");
  document.getElementById("mainPage").classList.remove("hidden");
  loadProfile();
  showSection("profileSection");
}
```

Penjelasan:

Fungsi ini berjalan setelah login berhasil.

Yang dilakukan:

1. Menyembunyikan halaman login.
2. Menampilkan halaman utama.
3. Memuat data profil.
4. Menampilkan bagian profil.

---

## 7. Fungsi Pindah Menu

```javascript
function showSection(sectionId) {
  document.getElementById("profileSection").classList.add("hidden");
  document.getElementById("editSection").classList.add("hidden");
  document.getElementById("passwordSection").classList.add("hidden");

  document.getElementById(sectionId).classList.remove("hidden");
}
```

Penjelasan:

Fungsi ini digunakan untuk berpindah menu.

Contohnya saat klik tombol Edit Profil:

```javascript
showSection("editSection")
```

Maka bagian edit profil akan ditampilkan, sedangkan bagian lain disembunyikan.

---

## 8. Fungsi Load Profil

```javascript
function loadProfile() {
  const data = JSON.parse(localStorage.getItem("profileData"));

  document.getElementById("viewNama").innerText = data.nama;
  document.getElementById("viewKelas").innerText = data.kelas;
  document.getElementById("viewJurusan").innerText = data.jurusan;
}
```

Penjelasan:

Fungsi ini digunakan untuk mengambil data profil dari `localStorage`, lalu menampilkannya ke halaman profil.

Karena data di `localStorage` berbentuk teks, maka harus diubah kembali menjadi object menggunakan:

```javascript
JSON.parse()
```

---

## 9. Fungsi Simpan Profil

```javascript
function saveProfile() {
  const profile = {
    nama: document.getElementById("nama").value,
    kelas: document.getElementById("kelas").value,
    jurusan: document.getElementById("jurusan").value,
    alamat: document.getElementById("alamat").value,
    sekolah: document.getElementById("sekolah").value,
    alamatSekolah: document.getElementById("alamatSekolah").value,
    website: document.getElementById("website").value
  };

  localStorage.setItem("profileData", JSON.stringify(profile));
  loadProfile();

  showMessage("profileMessage", "Profil berhasil disimpan!", "success");
  showSection("profileSection");
}
```

Penjelasan:

Fungsi ini digunakan untuk menyimpan data profil yang diisi dari form.

Langkah kerjanya:

1. Mengambil data dari form.
2. Menggabungkan data menjadi object `profile`.
3. Menyimpan data ke `localStorage`.
4. Memuat ulang data profil.
5. Menampilkan pesan berhasil.
6. Kembali ke halaman profil.

---

## 10. Fungsi Ubah Password

```javascript
function changePassword() {
  const oldPassword = document.getElementById("oldPassword").value;
  const newPassword = document.getElementById("newPassword").value;
  const confirmPassword = document.getElementById("confirmPassword").value;
  const savedPassword = localStorage.getItem("loginPassword");

  if (oldPassword !== savedPassword) {
    showMessage("passwordMessage", "Password lama salah!", "error");
    return;
  }

  if (newPassword.length < 4) {
    showMessage("passwordMessage", "Password baru minimal 4 karakter!", "error");
    return;
  }

  if (newPassword !== confirmPassword) {
    showMessage("passwordMessage", "Konfirmasi password tidak sama!", "error");
    return;
  }

  localStorage.setItem("loginPassword", newPassword);

  showMessage("passwordMessage", "Password berhasil diubah!", "success");
}
```

Penjelasan:

Fungsi ini digunakan untuk mengganti password.

Validasi yang dilakukan:

| Validasi | Penjelasan |
|---|---|
| Password lama harus benar | Agar tidak sembarang orang mengganti password |
| Password baru minimal 4 karakter | Agar password tidak terlalu pendek |
| Konfirmasi password harus sama | Agar tidak salah mengetik password baru |

Jika semua benar, password baru akan disimpan ke:

```javascript
localStorage.setItem("loginPassword", newPassword);
```

---

## 11. Fungsi Menampilkan Pesan

```javascript
function showMessage(id, text, type) {
  const message = document.getElementById(id);
  message.innerText = text;
  message.className = "message " + type;
  message.style.display = "block";

  setTimeout(function() {
    message.style.display = "none";
  }, 3000);
}
```

Penjelasan:

Fungsi ini digunakan untuk menampilkan pesan seperti:

- Login salah
- Profil berhasil disimpan
- Password berhasil diubah
- Password lama salah

Pesan akan tampil selama 3 detik, lalu hilang otomatis.

Bagian ini:

```javascript
setTimeout(function() {
  message.style.display = "none";
}, 3000);
```

Artinya pesan akan disembunyikan setelah 3000 milidetik atau 3 detik.

---

## 12. Cek Status Login

```javascript
if (localStorage.getItem("isLogin") === "true") {
  showMainPage();
}
```

Penjelasan:

Kode ini digunakan agar jika pengguna sudah login sebelumnya, maka saat halaman dibuka lagi pengguna langsung masuk ke halaman utama.

Jika belum login, maka tetap tampil halaman login.

---

# Penjelasan localStorage

`localStorage` adalah tempat penyimpanan data di browser.

Data yang disimpan di project ini adalah:

| Nama Data | Fungsi |
|---|---|
| `loginPassword` | Menyimpan password login |
| `profileData` | Menyimpan data profil siswa dan sekolah |
| `isLogin` | Menyimpan status apakah user sedang login |

Contoh menyimpan data:

```javascript
localStorage.setItem("loginPassword", "1234567@888");
```

Contoh mengambil data:

```javascript
localStorage.getItem("loginPassword");
```

Contoh menghapus data:

```javascript
localStorage.removeItem("isLogin");
```

Contoh menghapus semua data:

```javascript
localStorage.clear();
```

---

# Kelebihan Website

Website ini memiliki beberapa kelebihan:

1. Mudah dibuat.
2. Tidak membutuhkan database.
3. Tidak membutuhkan server khusus.
4. Bisa dijalankan langsung dari browser.
5. Bisa di-hosting gratis menggunakan GitHub Pages.
6. Cocok untuk belajar dasar HTML, CSS, dan JavaScript.

---

# Kekurangan Website

Karena website ini masih sederhana, ada beberapa kekurangan:

1. Data hanya tersimpan di browser.
2. Jika dibuka dari laptop lain, data bisa berbeda.
3. Jika cache atau localStorage browser dihapus, data akan hilang.
4. Password belum aman karena masih tersimpan di browser.
5. Website ini belum cocok untuk sistem login asli.
6. Website ini belum menggunakan database.

---

# Catatan Keamanan

Website ini hanya digunakan untuk tugas sekolah dan pembelajaran.

Sistem login pada website ini belum aman untuk penggunaan nyata karena:

- Password disimpan di browser.
- Tidak ada enkripsi password.
- Tidak ada database.
- Tidak ada server backend.

Untuk sistem sungguhan, sebaiknya menggunakan:

- Database
- Backend seperti PHP, Node.js, atau Laravel
- Password yang di-hash
- Validasi keamanan yang lebih lengkap

---

# Cara Reset Password Jika Lupa

Jika lupa password, password bisa di-reset dari browser.

Langkahnya:

1. Buka website.
2. Klik kanan pada halaman.
3. Pilih **Inspect**.
4. Masuk ke tab **Console**.
5. Ketik:

```javascript
localStorage.clear();
```

6. Tekan Enter.
7. Refresh halaman.
8. Login kembali menggunakan password default.

---

# Kesimpulan

Website ini adalah website profil siswa sederhana yang dibuat menggunakan HTML, CSS, dan JavaScript.

Website ini memiliki fitur login, profil siswa, edit profil, ubah password, dan logout.

Data disimpan menggunakan `localStorage`, sehingga website tidak membutuhkan database.

Project ini cocok digunakan sebagai tugas sekolah karena membantu memahami dasar pembuatan website dari awal sampai bisa online menggunakan GitHub Pages.

---

# Materi yang Dipelajari

Dari project ini, saya belajar:

1. Membuat struktur halaman menggunakan HTML.
2. Mengatur tampilan menggunakan CSS.
3. Membuat fungsi login menggunakan JavaScript.
4. Mengambil data dari form input.
5. Menampilkan data ke halaman website.
6. Menyimpan data menggunakan localStorage.
7. Membuat fitur ubah password sederhana.
8. Membuat website responsive.
9. Mengupload website ke GitHub.
10. Menjalankan website online dengan GitHub Pages.

---

# Dibuat Oleh

Project ini dibuat untuk tugas sekolah SMK.

```text
Nama    : [Isi Nama Siswa]
Kelas   : [Isi Kelas]
Jurusan : [Isi Jurusan]
Sekolah : [Isi Nama Sekolah]
```
