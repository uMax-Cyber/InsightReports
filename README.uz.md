<div align="center">

[![English](https://img.shields.io/badge/README-English-blue)](README.md)
[![Русский](https://img.shields.io/badge/README-Русский-red)](README.ru.md)
[![Oʻzbekcha](https://img.shields.io/badge/README-Oʻzbekcha-green)](README.uz.md)

</div>

# Qorongʻu temali animatsion hisobot shabloni
[![CI](https://github.com/uMax-Cyber/InsightReports/actions/workflows/ci.yml/badge.svg)](https://github.com/uMax-Cyber/InsightReports/actions/workflows/ci.yml)


![Namoyish](screenshots/demo.svg)
Qorongʻu tema, inline SVG animatsiyalar va muammolarning ichki vizualizatsiyalari bilan HTML hisobot generatori. Har bir muammo «oldin/keyin» animatsiya juftligini oladi — istalgan brauzerda ishlaydi, tashqi fayllar kerak emas.

## ✨ Imkoniyatlar

- **Oʻz-oʻzidan toʻliq hisobotlar** — bitta HTML fayl, barcha SVG animatsiyalar inline, tashqi resurslarsiz
- **«Oldin/keyin» hikoyasi** — har bir muammo uchun buzilgan va tuzatilgan holatning animatsion vizualizatsiyasi tayyor
- **Qorongʻu dizayn tizimi** — oʻqilishi va status ranglari uchun sozlangan GitHub uslubidagi palitra
- **Nol bogʻliqlik** — sof HTML + CSS + SMIL, zamonaviy brauzerlarning barchasida ochiladi

## Dizayn tizimi

- **Palitra**: fon `#0d1117`, panellar `#161b22`, chegaralar `#30363d`, matn `#e6edf3`
- **Urgʻular**: koʻk `#58a6ff` (maʼlumot), qizil `#f85149` (muammo), yashil `#3fb950` (tuzatish), sariq `#d29922` (ogohlantirish)
- **Shriftlar**: tizimli toʻplam (Segoe UI / -apple-system / sans-serif)

## Animatsiya turlari (barchasi — SMIL bilan inline SVG)

| Animatsiya | CSS/SMIL | Qoʻllanilishi |
|-----------|----------|----------|
| fadeUp | `@keyframes` | Kartochkalarning paydo boʻlishi |
| grow | `@keyframes` | Progress-panelning toʻldirilishi |
| pulse | `@keyframes` | Kritik ogohlantirishlarga eʼtibor jalb qilish |
| packet-flow | `<animate x>` | Tarmoq paketlarining harakati |
| counter | `<animate>` + JS (ixtiyoriy) | Raqamlarning oshib borishi |
| pool-grid | bosqichma-bosqich `<animate opacity>` | Status panjaralarining toʻldirilishi |

## Tuzilma

```
Report
├── Header (title, date, metadata)
├── "TL;DR" verdict block (3 key phrases)
├── Stat cards (big numbers, fadeUp animation)
├── Problem sections (each with SVG animation)
│   ├── Problem description
│   ├── Animated SVG visualization ("before")
│   └── Fix section
│       └── Animated SVG visualization ("after")
├── Findings table
└── Action plan (numbered steps)
```

## Misol: DHCP pul tugashi (inline SVG)

Vizualizada koʻrsatiladi:
- Mijoz 📱 serverga DISCOVER paketlarini yuboradi
- Server 😕 (qizil) pul toʻlganda ularni eʼtiborsiz qoldiradi
- Pul panjarasi: 38/40 kvadrat qizil (bosqichma-bosqich shaffoflik animatsiyasi)
- Tuzatilgandan soʻng: server 😀 (yashil), OFFER paketlari qaytadi, pul 15/40

## Foydalanish

```bash
# Shablonni nusxalab, mazmunini almashtiring
cp templates/report_dark_20260909.html my-report.html
# Boʻlimlarni oʻz maʼlumotlaringizga moslab tahrirlang
# Brauzerda oching — animatsiyalar avtomatik ishga tushadi
```

## Litsenziya
MIT

## 📬 Aloqa

Savollaringiz bormi? Yozing: **[allumaxmail@gmail.com](mailto:allumaxmail@gmail.com)**

---

<div align="center">

[![English](https://img.shields.io/badge/README-English-blue)](README.md)
[![Русский](https://img.shields.io/badge/README-Русский-red)](README.ru.md)
[![Oʻzbekcha](https://img.shields.io/badge/README-Oʻzbekcha-green)](README.uz.md)

</div>
