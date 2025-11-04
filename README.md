<!-- Al-Quran JSON Library -->
<div align="center" style="font-family:'Segoe UI',sans-serif;color:#083927;">
  <img src="https://github.com/Habibzz01/XbibzAssets-/releases/download/Nexo444/mylogobulat.png" width="120" style="border-radius:50%;box-shadow:0 0 12px rgba(5,77,64,0.25);" />
  <h1 style="margin-top:8px;color:#106c4f;">Al-Qur'an JSON Library</h1>
  <p style="color:#0b6b56;">Library modern untuk memuat teks Arab Uthmani + terjemahan multi-bahasa</p>
  <p>
    <img src="https://img.shields.io/badge/npm-alquran-orange?logo=npm" />
    <img src="https://img.shields.io/badge/jsDelivr-CDN-blue?logo=jsdelivr" />
    <img src="https://img.shields.io/badge/license-MIT-green" />
  </p>
</div>

---

## 🌿 Overview
Library **Al-Qur'an JSON** berisi teks Arab Uthmani, juz, surah, ayat, dan terjemahan multi-bahasa.
Didesain agar ringan dan mudah diakses baik lewat **CDN (jsDelivr)** maupun **npm (Node.js)**.

---

## 🚀 Cara Penggunaan

### 🧭 1. Menggunakan CDN (Browser)
```html
<script type="module">
async function loadQuran() {
  const res = await fetch("https://github.com/XbibzOfficial777/XbibzAlquranLibrary/releases/download/v1.0/alquran.json");
  const data = await res.json();
  console.log("Total Surah:", data.content.surahs.length);

  // Contoh: ambil Surah Al-Fatihah ayat pertama
  const fatihah = data.content.surahs.find(s => s.number === 1);
  console.log("Surah:", fatihah.name, "→", fatihah.ayahs[0].text);
}
loadQuran();
</script>
```

---

### 💻 2. Menggunakan Node.js / Deno / Bun
```bash
npm install alquran
```
Lalu:
```js
import fs from "fs";
const quran = JSON.parse(fs.readFileSync("./node_modules/@xbibzlibrary/alquran/dist/alquran.json", "utf8"));
console.log("Surah count:", quran.content.surahs.length);
```
Atau fetch langsung:
```js
import fetch from "node-fetch";
const res = await fetch("https://github.com/XbibzOfficial777/XbibzAlquranLibrary/releases/download/v1.0/alquran.json");
const data = await res.json();
console.log(data.content.surahs[0].ayahs[0].text);
```

---

## ⚙️ Struktur Data JSON (Singkat)
```json
{
  "generated_at": "...",
  "content": {
    "surahs": [
      {
        "number": 1,
        "name": "Al-Fatihah",
        "ayahs": [
          {
            "numberInSurah": 1,
            "text": "بِسْمِ اللَّهِ الرَّحْمَٰنِ الرَّحِيمِ",
            "translations": { "id": "Dengan nama Allah...", "en": "In the name of Allah..." }
          }
        ]
      }
    ]
  }
}
```

---

## 🌐 CDN & NPM Reference
- **CDN:** [GitHub Release](https://github.com/XbibzOfficial777/XbibzAlquranLibrary/releases)
- **npm:** [`@xbibzlibrary/alquran`](https://www.npmjs.com/package/@xbibzlibrary/alquran)

---

## 🧾 License
MIT © Xbibz Official
