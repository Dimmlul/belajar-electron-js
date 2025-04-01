

---

## 🚀 **1. Buat Proyek Electron + React + Vite**
Buka terminal dan jalankan:
```bash
npm create vite@latest
```
**Saat ditanya, pilih opsi berikut:**
1. **Project name:** `electronJS` *(atau sesuai keinginan)*
2. **Package name:** `electronjs`
3. **Select a framework:** **Others**
4. **Select a variant:** **Electron ↗**  
   *(Akan menginstall `create-electron-vite` secara otomatis)*
5. Konfirmasi instalasi: **ketik `y` dan tekan Enter**  

---

## 🚀 **2. Masuk ke Folder Proyek**
Setelah proses pembuatan selesai, jalankan:
```bash
cd electronJS
```

---

## 🚀 **3. Install Dependensi**
Jalankan:
```bash
npm install
```
*(Akan menginstall semua paket yang diperlukan, termasuk Electron, React, dan Vite.)*

---

## 🚀 **4. Jalankan Aplikasi**
Jalankan:
```bash
npm run dev
```
Jika berhasil, **Electron akan terbuka** dengan tampilan React.  
Di terminal akan muncul:
```
VITE v5.x.x  ready in xxx ms

  ➜  Local:   http://localhost:5173/
  ➜  Network: use --host to expose
```

---

## 🚀 **5. Struktur Folder yang Terbentuk**
Setelah dijalankan, proyek akan memiliki struktur seperti ini:
```
electronJS/
│── dist-electron/       # Hasil build untuk Electron
│── node_modules/        # Dependensi proyek
│── public/              # File statis
│── src/                 # Source code React
│   ├── App.tsx          # Komponen utama React
│   ├── main.tsx         # Entry point React
│   ├── preload.ts       # Preload script untuk komunikasi antara Electron & React
│── electron/            # Folder utama Electron
│   ├── main.ts          # Main Process Electron
│   ├── preload.ts       # Bridge ke Renderer
│── .gitignore           # File untuk mengabaikan git
│── index.html           # Entry point HTML
│── package.json         # Konfigurasi proyek
│── tsconfig.json        # Konfigurasi TypeScript
│── vite.config.ts       # Konfigurasi Vite
```

---

## 🚀 **6. Konfigurasi Tambahan di `package.json`**
Buka `package.json` dan pastikan bagian **`"scripts"`** seperti ini:
```json
"scripts": {
  "dev": "vite",
  "build": "vite build",
  "start": "electron .",
  "electron:dev": "npm run dev & electron ."
}
```

---

## 🚀 **7. Build Aplikasi Electron**
Jika ingin membuat file **.exe (Windows) / .app (Mac) / Linux**, jalankan:
```bash
npm run build
```
File hasil build akan berada di dalam folder `dist-electron/`.

---

## 🚀 **8. Troubleshooting**
Jika aplikasi **tidak terbuka**, coba:
1. Pastikan tidak ada error di terminal saat menjalankan `npm run dev`
2. Jika aplikasi hanya menampilkan **halaman kosong**, coba:
   ```bash
   npm run electron:dev
   ```
3. Jika ada error `vite not found`, pastikan **Vite sudah terinstall** dengan:
   ```bash
   npm install vite --save-dev
   ```
   
---

🔥 **Sekarang proyek Electron + React + Vite kamu sudah siap!**  
Kalau ada error, kirimkan log error-nya supaya bisa kita perbaiki. 🚀