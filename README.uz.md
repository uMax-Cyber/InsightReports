<div align="center">

[![English](https://img.shields.io/badge/README-English-blue)](README.md)
[![Русский](https://img.shields.io/badge/README-Русский-red)](README.ru.md)
[![Oʻzbekcha](https://img.shields.io/badge/README-Oʻzbekcha-green)](README.uz.md)

</div>

# Qorongʻu temali animatsion hisobot shabloni
[![CI](https://github.com/uMax-Cyber/InsightReports/actions/workflows/ci.yml/badge.svg)](https://github.com/uMax-Cyber/InsightReports/actions/workflows/ci.yml)


![Namoyish](screenshots/demo.svg)
HTML hisobot generatori: qorongʻu tema, inline SVG animatsiyalar va har bir muammoning oʻz vizualizatsiyasi. Har bir muammo «oldin/keyin» juftligida koʻrsatiladi — hisobot har qanday brauzerda ochiladi va hech qanday tashqi fayl talab qilmaydi.

## ✨ Imkoniyatlar

- **Hammasi bitta faylda** — barcha SVG animatsiyalar HTML ichiga joylangan, tashqi resurs kerak emas
- **«Oldin/keyin» uslubi** — har bir muammo uchun buzilgan hamda tuzatilgan holatning animatsiyasi tayyor turadi
- **Qorongʻu dizayn tizimi** — oʻqishga qulay, GitHub uslubidagi palitra va status ranglari
- **Tashqi kutubxonasiz** — sof HTML + CSS + SMIL, zamonaviy brauzerda bemalol ochiladi

## Dizayn tizimi

- **Palitra**: fon `#0d1117`, panellar `#161b22`, chegaralar `#30363d`, matn `#e6edf3`
- **Urgʻu ranglar**: koʻk `#58a6ff` (maʼlumot), qizil `#f85149` (muammo), yashil `#3fb950` (tuzatish), sariq `#d29922` (ogohlantirish)
- **Shriftlar**: tizim shriftlari (Segoe UI / -apple-system / sans-serif)

## Animatsiya turlari (barchasi — SMIL bilan inline SVG)

| Animatsiya | CSS/SMIL | Qoʻllanilish holati |
|-----------|----------|----------|
| fadeUp | `@keyframes` | Kartochkalar paydo boʻladi |
| grow | `@keyframes` | Progress barlar toʻladi |
| pulse | `@keyframes` | Kritik ogohlantirish diqqatni tortadi |
| packet-flow | `<animate x>` | Tarmoq paketlari harakatlanadi |
| counter | `<animate>` + JS (ixtiyoriy) | Raqamlar hisoblanib boradi |
| pool-grid | bosqichma-bosqich `<animate opacity>` | Status panjarasi kataklari ketma-ket yonadi |

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

## Misol: DHCP pool tugashi (inline SVG)

Vizualizatsiya quyidagilarni koʻrsatadi:
- Mijoz 📱 server tomon DISCOVER paketlarini yuboradi
- IP manzillar qolmagach, server 😕 (qizil) ularni javobsiz qoldiradi
- Pool panjarasi: 38/40 katak qizil (kataklar ketma-ket yonadi)
- Tuzatilgandan keyin: server 😀 (yashil), OFFER paketlari qaytadi, poolda 15/40 band

## Foydalanish

```bash
# Shablonni nusxalab, mazmunini oʻz maʼlumotlaringizga moslang
cp templates/report_dark_20260909.html my-report.html
# Brauzerda oching — animatsiyalar oʻzi ishga tushadi
```

## Litsenziya
MIT

## 📬 Aloqa

Savollaringiz boʻlsa yozing: **[allumaxmail@gmail.com](mailto:allumaxmail@gmail.com)**

---

<div align="center">

[![English](https://img.shields.io/badge/README-English-blue)](README.md)
[![Русский](https://img.shields.io/badge/README-Русский-red)](README.ru.md)
[![Oʻzbekcha](https://img.shields.io/badge/README-Oʻzbekcha-green)](README.uz.md)

</div>
