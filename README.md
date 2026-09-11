# Web-TESSA

**Project manager :** Muhammad Zaki Syauqi  
**Front-End :**  
- as
- as

**Back-End :**
- as
- as

**UI/UX :**
- Azril Aziza
- Firza Fahlevi  

**Tester :**  
- Nadzli Dhea Syahrani
- ad


## PRD
# Product Requirements Document (PRD)

## Website Organisasi & Event Registration

### 1. Product Overview

Website ini merupakan platform resmi organisasi yang berfungsi sebagai pusat informasi organisasi, dokumentasi kegiatan, serta sistem pendaftaran kegiatan/event.

Website terdiri dari tiga fungsi utama:

1. **Home** — memperkenalkan organisasi kepada pengunjung.
2. **Gallery** — menampilkan dokumentasi kegiatan organisasi.
3. **Event** — menampilkan kegiatan yang sedang atau akan diselenggarakan serta menyediakan sistem pendaftaran.

Pengunjung tidak diwajibkan memiliki akun untuk melihat informasi organisasi, gallery, maupun daftar event. **Login hanya diperlukan ketika pengguna ingin melakukan pendaftaran event.**

Sistem pembayaran event menggunakan **transfer manual**, bukan payment gateway. Setelah melakukan transfer, peserta mengunggah bukti pembayaran dan admin melakukan verifikasi secara manual.

---

# 2. Problem Statement

Informasi mengenai organisasi, dokumentasi kegiatan, dan event sering kali tersebar di berbagai platform seperti Instagram, WhatsApp, dan Google Forms.

Hal tersebut dapat menyebabkan:

* Informasi organisasi sulit ditemukan secara terpusat.
* Dokumentasi kegiatan tidak tersusun dengan baik.
* Informasi event tidak memiliki tempat khusus.
* Proses pendaftaran event masih dilakukan secara manual.
* Admin kesulitan mengelola data peserta.
* Verifikasi pembayaran sulit dilakukan jika menggunakan banyak platform berbeda.

Website ini dibuat untuk menyediakan satu platform yang mengintegrasikan informasi organisasi, dokumentasi, event, pendaftaran, dan verifikasi pembayaran.

---

# 3. Goals

### Primary Goals

* Menyediakan website resmi organisasi.
* Memperkenalkan identitas, visi, misi, dan divisi organisasi.
* Menyediakan gallery dokumentasi kegiatan.
* Menampilkan informasi event secara terstruktur.
* Memudahkan peserta melakukan pendaftaran event.
* Memudahkan admin mengelola peserta.
* Menyediakan sistem pembayaran manual yang tetap dapat diverifikasi.

### Secondary Goals

* Mengurangi ketergantungan terhadap Google Forms untuk pendaftaran.
* Menyimpan data peserta secara terstruktur.
* Membuat riwayat pendaftaran peserta dapat dilihat kembali.

---

# 4. Target Users

### Guest

Pengunjung yang hanya ingin melihat informasi organisasi.

Guest dapat:

* Membuka Home.
* Melihat visi dan misi.
* Melihat divisi organisasi.
* Melihat Gallery.
* Melihat daftar Event.
* Melihat detail Event.

Guest tidak dapat:

* Melakukan pendaftaran event.
* Melihat riwayat pendaftaran.

### Registered User

Pengguna yang telah memiliki akun.

User dapat:

* Melakukan login.
* Melihat profil.
* Mendaftar event.
* Melakukan pembayaran manual.
* Mengupload bukti pembayaran.
* Melihat status pendaftaran.
* Melihat riwayat pendaftaran.

### Admin

Pengelola website dan event.

Admin dapat:

* Mengelola informasi organisasi.
* Mengelola gallery.
* Membuat event.
* Mengubah event.
* Menghapus event.
* Melihat peserta.
* Memverifikasi pembayaran.
* Mengubah status pendaftaran.

---

# 5. Scope

## In Scope

* Organization profile.
* Vision & mission.
* Division information.
* Gallery.
* Event listing.
* Event detail.
* Authentication.
* Event registration.
* Manual payment.
* Upload payment proof.
* Payment verification.
* Registration status.
* Admin dashboard.

## Out of Scope

* Payment gateway.
* Automatic bank transaction verification.
* Automatic refund.
* E-wallet integration.
* Marketplace.
* Online ticket selling.

---

# 6. Information Architecture

```text
Website
│
├── Home
│   ├── Organization Introduction
│   ├── Vision
│   ├── Mission
│   └── Divisions
│
├── Gallery
│   ├── Gallery List
│   └── Gallery Detail
│
├── Event
│   ├── Event List
│   └── Event Detail
│       └── Registration
│
├── Authentication
│   ├── Login
│   └── Register
│
├── User Dashboard
│   ├── Profile
│   ├── My Registration
│   └── Payment Status
│
└── Admin Dashboard
    ├── Organization
    ├── Gallery
    ├── Events
    ├── Registrations
    └── Payment Verification
```

---

# 7. Home

Home merupakan halaman utama website.

### 7.1 Organization Introduction

Menampilkan penjelasan singkat mengenai organisasi.

Informasi:

* Nama organisasi.
* Logo.
* Deskripsi singkat.
* Tujuan organisasi.
* CTA menuju halaman informasi lebih lanjut jika diperlukan.

### 7.2 Vision

Menampilkan visi organisasi.

### 7.3 Mission

Menampilkan misi organisasi.

Misi dapat ditampilkan dalam bentuk beberapa poin.

### 7.4 Divisions

Menampilkan divisi yang terdapat dalam organisasi.

Setiap divisi memiliki:

* Nama divisi.
* Logo/icon atau foto.
* Deskripsi singkat.
* Tugas dan fungsi divisi.

---

# 8. Gallery

Gallery digunakan untuk menampilkan dokumentasi kegiatan organisasi.

### Gallery List

Setiap dokumentasi dapat memiliki:

* Foto.
* Judul kegiatan.
* Tanggal.
* Deskripsi singkat.
* Kategori kegiatan.

Contoh:

```text
Gallery
│
├── Seminar Nasional
├── Workshop
├── Bakti Sosial
├── Gathering
└── Kegiatan Internal
```

### Gallery Detail

Ketika pengguna memilih sebuah dokumentasi, sistem menampilkan:

* Judul.
* Tanggal.
* Deskripsi.
* Kumpulan foto kegiatan.

Gallery dapat menggunakan sistem pagination atau infinite scrolling apabila jumlah dokumentasi semakin banyak.

---

# 9. Event

Event merupakan halaman utama untuk kegiatan organisasi.

### Event List

Menampilkan event yang tersedia.

Informasi:

* Nama event.
* Thumbnail.
* Tanggal.
* Lokasi.
* Harga pendaftaran.
* Status pendaftaran.
* Sisa kuota jika diperlukan.

Event memiliki status:

```text
Upcoming
Open Registration
Full
Closed
Finished
```

### Event Detail

Menampilkan:

* Nama event.
* Poster.
* Deskripsi.
* Tanggal.
* Waktu.
* Lokasi.
* Pembicara jika ada.
* Benefit.
* Persyaratan.
* Harga.
* Kuota.
* Deadline pendaftaran.
* Informasi pembayaran.
* Tombol "Daftar".

---

# 10. Authentication

Authentication hanya diperlukan untuk pengguna yang ingin melakukan pendaftaran event.

### Guest

Guest dapat melihat event tanpa login.

Ketika menekan tombol:

```text
Daftar Event
```

sistem memeriksa status authentication.

Jika belum login:

```text
Anda harus login terlebih dahulu untuk mendaftar.
[Login]
[Register]
```

Setelah login berhasil, user diarahkan kembali ke halaman event yang ingin didaftarkan.

### Register

Data minimum:

* Nama.
* Email.
* Password.

Data tambahan dapat dikumpulkan ketika melakukan pendaftaran event.

### Login

User dapat login menggunakan:

* Email.
* Password.

### Logout

User dapat keluar dari akun.

---

# 11. Event Registration

Pendaftaran dilakukan setelah user login.

Form pendaftaran dapat disesuaikan dengan kebutuhan event.

Contoh:

* Nama lengkap.
* NIM.
* Program studi.
* Nomor telepon.
* Email.
* Pilihan bidang/divisi jika diperlukan.
* Alasan mengikuti event.
* Data tambahan sesuai kebutuhan event.

Setelah form dikirim, sistem membuat registration record.

Status awal:

```text
WAITING_PAYMENT
```

Jika event gratis:

```text
REGISTERED
```

---

# 12. Sistem Pembayaran Tanpa Payment Gateway

## Konsep

Sistem tidak melakukan transaksi pembayaran secara otomatis.

Alurnya:

```text
User
 ↓
Daftar Event
 ↓
Sistem membuat Registration
 ↓
User mendapatkan instruksi pembayaran
 ↓
User melakukan transfer melalui Mobile Banking/ATM
 ↓
User mengupload bukti transfer
 ↓
Admin memeriksa bukti
 ↓
Admin menyetujui / menolak
 ↓
Status Registration berubah
```

### Payment Method

Admin menyediakan rekening organisasi/panitia.

Contoh informasi:

```text
Bank       : Bank XXX
Nomor Rek. : XXXXXXXX
Atas Nama  : Nama Organisasi
Nominal    : Rp50.000
```

Sebaiknya sistem menghasilkan **kode pembayaran unik** atau nominal unik agar admin lebih mudah mencocokkan transaksi.

Contoh:

```text
Harga event       : Rp50.000
Kode pembayaran   : 127
Total transfer    : Rp50.127
```

Namun nominal unik ini hanya merupakan alat bantu rekonsiliasi, **bukan bukti pembayaran otomatis**.

### Upload Bukti Pembayaran

User dapat mengupload:

* Screenshot transfer.
* Foto bukti transfer.
* PDF bukti transfer jika diperlukan.

Setelah upload:

```text
Payment Status:
WAITING_VERIFICATION
```

### Admin Verification

Admin melihat:

```text
Nama peserta
Event
Nominal
Tanggal upload
Bukti pembayaran
Status
```

Admin memiliki dua pilihan:

```text
[Approve]
[Reject]
```

Jika approve:

```text
Payment = PAID
Registration = CONFIRMED
```

Jika reject:

```text
Payment = REJECTED
Registration = PAYMENT_REQUIRED
```

User kemudian dapat mengupload bukti baru.

---

# 13. Registration Status

Status pendaftaran:

```text
PENDING
WAITING_PAYMENT
WAITING_VERIFICATION
CONFIRMED
REJECTED
CANCELLED
```

Contoh alur:

```text
PENDING
   ↓
WAITING_PAYMENT
   ↓
WAITING_VERIFICATION
   ↓
CONFIRMED
```

Jika bukti pembayaran ditolak:

```text
WAITING_VERIFICATION
          ↓
       REJECTED
          ↓
   Upload Bukti Baru
          ↓
WAITING_VERIFICATION
```

---

# 14. User Dashboard

User dashboard digunakan untuk melihat aktivitas pengguna.

### Profile

Menampilkan:

* Nama.
* Email.
* NIM.
* Program studi.
* Nomor telepon.

### My Registration

Menampilkan seluruh event yang pernah didaftarkan.

Contoh:

| Event      | Date   | Payment      | Registration |
| ---------- | ------ | ------------ | ------------ |
| Workshop A | 20 Sep | Paid         | Confirmed    |
| Seminar B  | 25 Sep | Verification | Waiting      |

### Payment

User dapat:

* Melihat instruksi pembayaran.
* Upload bukti.
* Melihat status verifikasi.
* Mengupload ulang jika ditolak.

---

# 15. Admin Dashboard

Admin dashboard menjadi pusat pengelolaan website.

### Organization Management

Admin dapat:

* Mengubah deskripsi organisasi.
* Mengubah visi.
* Mengubah misi.
* Menambah/mengubah/menghapus divisi.

### Gallery Management

Admin dapat:

* Upload foto.
* Membuat gallery.
* Mengubah gallery.
* Menghapus gallery.

### Event Management

Admin dapat:

* Membuat event.
* Mengedit event.
* Menghapus event.
* Membuka/menutup pendaftaran.
* Mengatur kuota.
* Mengatur harga.
* Mengatur rekening pembayaran.

### Registration Management

Admin dapat melihat:

* Nama peserta.
* Event.
* Data pendaftaran.
* Status pendaftaran.
* Status pembayaran.

### Payment Verification

Admin dapat:

* Melihat bukti transfer.
* Approve pembayaran.
* Reject pembayaran.
* Memberikan alasan penolakan.

---

# 16. Business Rules

### Authentication

1. Guest dapat melihat seluruh informasi publik.
2. User wajib login untuk melakukan pendaftaran.
3. User tidak dapat mendaftar event yang sama lebih dari satu kali.
4. User dapat melihat riwayat pendaftaran miliknya sendiri.
5. Admin memiliki akses ke dashboard administrasi.

### Event

1. Event yang sudah ditutup tidak dapat menerima pendaftaran baru.
2. Event yang sudah mencapai kuota tidak dapat menerima pendaftaran baru.
3. Event yang sudah selesai tidak dapat didaftarkan.
4. Admin dapat membuka atau menutup pendaftaran secara manual.

### Payment

1. Sistem tidak memproses transaksi secara otomatis.
2. User bertanggung jawab melakukan transfer ke rekening yang ditampilkan.
3. User wajib mengupload bukti pembayaran.
4. Pembayaran dianggap valid hanya setelah diverifikasi admin.
5. Admin dapat menolak bukti pembayaran.
6. Bukti pembayaran yang ditolak dapat diupload kembali.
7. User tidak boleh mengubah nominal pembayaran melalui form setelah registration dibuat.
8. Admin dapat melihat seluruh bukti pembayaran.

---

# 17. Data Requirements

Data utama yang diperlukan:

### Users

```text
id
name
email
password/auth_provider
role
created_at
updated_at
```

Role:

```text
USER
ADMIN
```

### Events

```text
id
title
description
poster
start_date
end_date
location
price
quota
registration_deadline
status
created_at
updated_at
```

### Registrations

```text
id
user_id
event_id
registration_data
status
created_at
updated_at
```

### Payments

```text
id
registration_id
amount
payment_method
payment_proof
status
verified_by
verified_at
rejection_reason
created_at
updated_at
```

### Gallery

```text
id
title
description
event_date
cover_image
created_at
updated_at
```

### Gallery Images

```text
id
gallery_id
image
created_at
```

---

# 18. Security Requirements

Sistem harus memastikan:

* Password tidak disimpan sebagai plaintext.
* User hanya dapat melihat data pendaftarannya sendiri.
* User tidak dapat mengakses dashboard admin.
* Admin harus melalui authentication.
* Upload file memiliki validasi format dan ukuran.
* File bukti pembayaran tidak boleh dapat diakses sembarang user.
* Registration tidak boleh dimanipulasi melalui perubahan parameter URL.
* Admin action harus memiliki authorization.
* Data pembayaran harus memiliki audit information seperti `verified_by` dan `verified_at`.

---

# 19. Non-Functional Requirements

### Responsive

Website harus dapat digunakan pada:

* Mobile.
* Tablet.
* Desktop.

Prioritas desain adalah **mobile-first**.

### Performance

* Image gallery harus dioptimasi.
* Lazy loading digunakan untuk gambar.
* Ukuran file upload dibatasi.
* Halaman event harus tetap cepat meskipun jumlah event bertambah.

### Availability

Website harus dapat diakses selama event dan periode pendaftaran.

### Usability

Pengguna harus dapat menemukan event dan melakukan pendaftaran tanpa navigasi yang membingungkan.

---

# 20. Acceptance Criteria

### Home

* Pengunjung dapat melihat informasi organisasi.
* Pengunjung dapat melihat visi dan misi.
* Pengunjung dapat melihat divisi.

### Gallery

* Pengunjung dapat melihat dokumentasi.
* Pengunjung dapat membuka detail gallery.
* Admin dapat menambah dan menghapus dokumentasi.

### Event

* Pengunjung dapat melihat event tanpa login.
* Pengunjung dapat melihat detail event.
* User dapat mendaftar setelah login.
* Sistem mencegah duplicate registration.
* Sistem menerapkan batas kuota.

### Payment

* User mendapatkan instruksi transfer.
* User dapat mengupload bukti pembayaran.
* Admin dapat melihat bukti.
* Admin dapat approve/reject pembayaran.
* User dapat melihat status pembayaran.
* User dapat melakukan upload ulang jika pembayaran ditolak.

---

# 21. Success Metrics

Keberhasilan website dapat diukur melalui:

* Jumlah pengunjung website.
* Jumlah user yang membuat akun.
* Jumlah pendaftaran event.
* Persentase pendaftaran yang berhasil dikonfirmasi.
* Jumlah event yang dikelola melalui website.
* Waktu yang dibutuhkan admin untuk memverifikasi pembayaran.
* Jumlah pendaftaran yang gagal akibat masalah sistem.

---

# 22. Future Development

Fitur berikut dapat dikembangkan kemudian:

* QR Code check-in peserta.
* E-ticket.
* Certificate generator.
* Email notification.
* WhatsApp notification.
* Export peserta ke Excel.
* Automatic reminder event.
* Dashboard statistik event.
* Payment gateway apabila organisasi sudah membutuhkannya.
