# Hasil Automation Testing (Maestro)

Berikut adalah ringkasan spreadsheet skenario pengujian otomatisasi menggunakan framework Maestro untuk aplikasi Work Fusion. Seluruh pengujian berjalan dengan lancar (Passed).

## Tabel Test Cases

| Test ID | Modul / Aktor | Skenario Pengujian | Detail Langkah (Steps) | Hasil yang Diharapkan (Expected Result) | Status |
|:---:|---|---|---|---|:---:|
| TC-01 | Auth (Worker) | Login Worker (Successful) | 1. Buka aplikasi<br>2. Ketuk "Continue to Work Fusion"<br>3. Masukkan username `rakha`<br>4. Masukkan password `Rakha123!`<br>5. Ketuk "Sign in" | Menampilkan *welcome text* `Hi, r ☀️ Welcome to Work Fusion!` dan masuk ke dashboard Worker. | Passed ✅ |
| TC-02 | Auth (Supervisor) | Login Supervisor (Successful) | 1. Buka aplikasi<br>2. Ketuk "Continue to Work Fusion"<br>3. Masukkan username `nailussaada`<br>4. Masukkan password `Nailus123!`<br>5. Ketuk "Sign in" | Menampilkan *welcome text* `Hi, Nailus ☀️ Welcome to Work Fusion!` dan berhasil masuk. | Passed ✅ |
| TC-03 | Auth (Worker) | Logout Worker dari Dashboard | 1. Login menggunakan akun Worker<br>2. Navigasi ke tab **Profile** (Tab 3)<br>3. Ketuk interaksi tombol **Log Out** | Sesi berakhir dan beralih ke layar awal/guest dengan teks `Hi, welcome to Work Fusion`. | Passed ✅ |
| TC-04 | Overview (Worker) | Filter Data berdasarkan Rentang Tanggal | 1. Ketuk ikon **Filter**<br>2. Pilih menu **Select date range**<br>3. Pilih rentang dari 11 April 2026 hingga 22 April 2026<br>4. Ketuk **Save** dan **Apply Filter** | Data tabel diperbarui dan menampilkan indikator rentang tanggal `Showing range (11 Apr 2026 - 22 Apr 2026)`. | Passed ✅ |
| TC-05 | Profile (Worker) | Edit Nama Profil Worker | 1. Navigasi menuju halaman **Profile**<br>2. Ketuk area pengeditan (koordinat dua kali klik di area 86%,16%) | UI merespons koordinat klik sehingga pengguna masuk ke dalam *editing constraint mode* profil. | Passed ✅ |

---

## Penjelasan Masing-Masing Test Case

### 1. `worker-login.yaml` (TC-01)
Skrip pengujian *happy-flow* dari fitur masuk log bagi aktor **Worker**. Aplikasi dijalankan pada sesi yang sepenuhnya bersih (*clear status: true*). Maestro mengotomatisasi interaksi masukan kata sandi secara rahasia dan memverifikasinya melalui asersi fungsional pada tampilan (`assertVisible`) guna membuktikan keabsahan akses untuk akun pengujian dengan *username* `rakha`.

### 2. `supervisor-login.yaml` (TC-02)
Pengujian mandiri identik dengan skenario Worker, namun dialokasikan bagi peran **Supervisor**. Skrip ini menjaga keamanan pengecekan otentikasi bahwa logika form masuk sistem membedakan antarmuka sapaan (`assertVisible` pada "Nailus") dan fungsionalitas kredensial dari profil yang dimuat, serta memastikan akses role lain dalam Work Fusion tidak rusak. 

### 3. `worker-logout.yaml` (TC-03)
Merupakan *end-to-end authentication test* untuk prosedur pembongkaran sesi keamanan (*loging out*). Digabung dari langkah login valid, lalu mengotomatisasi tap pada antarmuka "Tab Profile". Pengujian memuncak pada ketukan tombol *Logout* untuk memastikan *state* memori sistem dikosongkan dan dialihkan ulang menatap antarmuka layar utama pengunjung (`assertVisible`). 

### 4. `worker-overview-filter.yaml` (TC-04)
Pengujian navigasional komponen dalam *Stateful View* (halaman dasbor pekerja). Test ini secara proaktif mensimulasikan tap selektor kalender ganda (simulasi dua titik tanggal berbeda sekaligus). Penekanannya bukan pada database backend, namun validasi di hadapan User Interface dengan memastikan komponen antarmuka yang menunjukkan "Tampilan difilter berdasarkan kurun tanggal 11-22 Apr" berhasil dimunculkan merespon masukan button `Apply Filter`.

### 5. `worker-edit-profile-name.yaml` (TC-05)
Berbeda dengan skrip yang mencari teks eksak (String Identifier), *file test* ini menggunakan mekanisme Maestro merata-rata *screen boundary logic* dengan menggunakan perintah target presisi **point tap UI X,Y** berupa koordinat `86%,16%` (*Double tap execution*). Ini menunjukkan bagaimana otomasi berhasil diintegrasikan pada interaksi fisik ikon komponen, merangsang modul *profile inline editing mode* untuk reaktif.
