# 🧠 Git Flow & SDLC - Developer Workflow Guidelines

## 🚧 Branching Rules

- `main`: Branch **production**
- `dev`: Branch **development**
- `feat/<nama-fitur>`: Untuk pengembangan fitur
- `fix/<nama-bug>`: Untuk fix bug

---

## 🔁 Worflow Git

### ✅ Developer Flow

1. **Selalu start dari `dev`**

   ```
   git checkout dev
   git pull origin dev
   git checkout -b feature/nama-fitur
   ```
2. **Kerjakan kode di branch `feat/`**
3. **Sebelum push, WAJIB sinkronisasi untuk minimalkan konflik**

   ```
   git pull origin dev --rebase
   ```
4. **Push ke remote**

   ```bash
   git push origin feat/nama-fitur
   ```
5. **Buat Pull Request (PR) dari `feature/xxx` ke `dev`**

   * Gunakan judul & deskripsi PR yang informatif
   * Tambahkan referensi ke issue (jika ada)
   * Boleh self merge asalkan tidak ada conflict**
6. **Merge `dev` ke `main`**

   * Hanya dilakukan saat siap rilis

## ❌ Larangan

* ❌ Tidak boleh `push` langsung ke `main` atau `dev`
* ❌ Tidak boleh merge tanpa PR dan review
* ✅ Selalu lakukan `pull --rebase` sebelum push
* ✅ Semua perubahan WAJIB lewat Pull Request

---

## 📌 GitHub Issues

### Use GitHub Issues

* Report bug & error
* Request fitur baru

### Struktur Issue yang Disarankan

```md
## Ringkasan
Deskripsikan error/fitur secara singkat dan jelas.

## Langkah Reproduksi (untuk bug)
1. Langkah 1
2. Langkah 2
3. Error muncul di step ini

## Ekspektasi
Apa yang seharusnya terjadi?

## Catatan Tambahan
Tambahkan log error, screenshot, atau info pendukung lainnya.
```

### Assign ke Tim Relevan

* `@Mas-Alvi` → Backend (Mokoto / Rust)
* `@Mas-Manuel` → Frontend (React)
* `@Mas-Angga` → DevOps / Infrastruktur

### Labeling Issue

* `bug`
* `feature`
* `documentation`
* `urgent`
* `enhancement`

### PR Link ke Issue

Tambahkan di deskripsi PR:

```md
Closes #<nomor-issue>
```

Agar issue otomatis tertutup saat PR di-merge.

---

## 📦 Software Development Life Cycle (SDLC)

### 1. Planning

* Kebutuhan dikumpulkan dari stakeholder
* User story, use case, dan estimasi waktu dibuat

### 2. Analysis

* Breakdown sistem
* Tentukan arsitektur, stack, dan dependensi
* Issue GitHub dibuat berdasarkan task teknis

### 3. Design

* UI/UX mockup (bila perlu)
* API contract, DB schema, dan diagram alur sistem

### 4. Implementation

* Buat branch `feature/xxx`
* Coding sesuai flow PR
* Review & merge via Pull Request

### 5. Testing

* Unit test, integration test
* UAT (User Acceptance Testing)

### 6. Deployment

* Merge `dev` → `main` jika siap produksi
* CI/CD otomatis deploy ke staging atau production

### 7. Maintenance

* Monitoring sistem
* Bugfix lewat branch `hotfix/xxx` atau `bugfix/xxx`
* Iterasi & perbaikan berkelanjutan

---

## 👥 Tim Teknis

* **Mas Alvi** – Backend (Mokoto / Rust)
* **Mas Manuel** – Frontend (React)
* **Mas Angga** – DevOps / Infra

# Internal Core Flow

1. **Principal Awal (Client)**

   - Memiliki tanah
   - 1 meter = 1 token RWAC
2. **Tanah**

   - Aset fisik yang akan di-tokenisasi
3. **Tanah => Token**

   - Tokenisasi tanah berdasarkan luas
   - Konversi: `1 token = 1 meter`
4. **Jual per Token**

   - Token bisa dijual sebagian atau seluruhnya
5. **Beli Sebagian atau Semua?**

   - Pembeli bisa membeli token sesuai kebutuhan
6. **TOKEN Platform (Exchange)**

   - Token diperdagangkan di platform exchange
7. **Principal Baru (Client)**

   - Pembeli token menjadi pemilik baru

````