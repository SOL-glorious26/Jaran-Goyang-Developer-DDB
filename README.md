# Diponegoro Digital Bank (DDB)

Aplikasi bank digital **simulasi** (tanpa uang sungguhan) untuk mata kuliah Software Engineering, UKSW.
Dikerjakan oleh **Kelompok Jaran Goyang**, periode 15 September – 23 November 2026.

Aplikasi **Android** dan **Web** memakai **satu backend** yang sama, sehingga saldo dan riwayat selalu sinkron.

| Bagian | Teknologi | Folder |
|---|---|---|
| Android | Kotlin, Jetpack Compose, MVVM, Retrofit | `code_area/apps/android` |
| Web | Node.js, Express, EJS | `code_area/apps/web/digitalbanking-node` |
| Backend | Java 21, Spring Boot, PostgreSQL (H2 untuk uji cepat) | `code_area/backend` |
| Pengujian | Skrip uji sistem Android, Web, dan lintas platform beserta buktinya | `code_area/pengujian` |
| Dokumen | 9 dokumen proyek (Word dan PDF) | `documents_area` |
| Presentasi | Materi presentasi | `Presentasi` |

## Dokumen

| No | Dokumen |
|---|---|
| 1 | Project Document |
| 2 | Architectural Design |
| 3 | Functional Design |
| 4 | Detailed Design (4A Android, 4B Backend & Database, 4C Web) |
| 5 | User Interface Map (5A Android, 5B Web) |
| 6 | Pengujian Sistem (System Testing) |
| 7 | Developer Manual (7A Android, 7B Backend, 7C Web) |
| 8 | Demo Program Sistem (8A Android, 8B Web) |
| 9 | User Manual (9A Android, 9B Web) |

## Menjalankan

Kebutuhan: JDK 21 (sudah termasuk di Android Studio), Android Studio, dan Node.js 18 ke atas.

**1. Backend** (port 8080, database H2, tanpa perlu memasang PostgreSQL)

```powershell
cd code_area\backend
powershell -ExecutionPolicy Bypass -File .\run-local.ps1 -H2
```

**2. Android**

- Buka folder `code_area/apps/android` di Android Studio.
- Pilih varian **demoDebug** untuk mencoba tanpa backend, atau **onlineDebug** untuk terhubung ke backend.
- Jalankan di emulator (contoh: Pixel 8, API 37). Emulator otomatis memakai alamat backend `http://10.0.2.2:8080/`.

**3. Web** (port 3000, backend harus sudah jalan)

```powershell
cd code_area\apps\web\digitalbanking-node
copy .env.example .env
npm install
npm start
```

Lalu buka http://localhost:3000.

## Akun demo

| Username | Password | PIN transaksi |
|---|---|---|
| `demo` | `Demo@1234` | `123456` |

## Tim Android

| NIM | Anggota | Peran | Modul (PIC) |
|---|---|---|---|
| 622024022 | Salomo Putra Glorious Hokoyoku | Project Manager, Mobile Lead, Backend | Authentication, Virtual Card |
| 622024019 | Cecilia Adelaide Penlaana | Mobile Developer | Transfer, History & Dashboard |
| 622024006 | Gracia Riyanto | Mobile Developer | Payment (QRIS), Profile & Notification |
| 622024010 | Grace | Mobile Developer | Account, Top-up |

## Tim Web

| NIM | Anggota |
|---|---|
| 622024003 | Steven Wibisana |
| 622024005 | Rafi Fadhillah |
| 622024008 | Nabila P. A. |
| 622024016 | Permata Surya C. |

Rincian pembagian kerja ada di dokumen 1 (Project Document).
