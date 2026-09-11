<div align="center">

[![English](https://img.shields.io/badge/README-English-blue)](README.md)
[![Русский](https://img.shields.io/badge/README-Русский-red)](README.ru.md)
[![Oʻzbekcha](https://img.shields.io/badge/README-Oʻzbekcha-green)](README.uz.md)

</div>

# Шаблон анимированных отчётов в тёмной теме
[![CI](https://github.com/uMax-Cyber/InsightReports/actions/workflows/ci.yml/badge.svg)](https://github.com/uMax-Cyber/InsightReports/actions/workflows/ci.yml)


![Демонстрация](screenshots/demo.svg)
Генератор HTML-отчётов с тёмной темой, inline SVG-анимациями и встроенными визуализациями проблем. Каждая проблема получает пару анимаций «до/после» — воспроизводится в любом браузере, внешние файлы не нужны.

## ✨ Возможности

- **Самодостаточные отчёты** — один HTML-файл со всеми SVG-анимациями inline, без внешних ресурсов
- **Подача «до/после»** — для каждой проблемы готова анимированная визуализация сломанного и исправленного состояния
- **Тёмная дизайн-система** — палитра в стиле GitHub, настроенная на читаемость и статусные цвета
- **Ноль зависимостей** — чистые HTML + CSS + SMIL, открывается в любом современном браузере

## Дизайн-система

- **Палитра**: фон `#0d1117`, панели `#161b22`, рамки `#30363d`, текст `#e6edf3`
- **Акценты**: синий `#58a6ff` (информация), красный `#f85149` (проблема), зелёный `#3fb950` (исправление), жёлтый `#d29922` (предупреждение)
- **Шрифты**: системный стек (Segoe UI / -apple-system / sans-serif)

## Типы анимаций (все — inline SVG со SMIL)

| Анимация | CSS/SMIL | Сценарий применения |
|-----------|----------|----------|
| fadeUp | `@keyframes` | Появление карточек |
| grow | `@keyframes` | Заполнение прогресс-баров |
| pulse | `@keyframes` | Привлечение внимания к критическим алертам |
| packet-flow | `<animate x>` | Движение сетевых пакетов |
| counter | `<animate>` + JS опционально | Счётчики, бегущие вверх |
| pool-grid | ступенчатый `<animate opacity>` | Заполнение статусных сеток |

## Структура

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

## Пример: исчерпание пула DHCP (inline SVG)

Визуализация показывает:
- Клиент 📱 отправляет пакеты DISCOVER в сторону сервера
- Сервер 😕 (красный) игнорирует их, когда пул заполнен
- Сетка пула: 38/40 квадратов красные (ступенчатая анимация прозрачности)
- После исправления: сервер 😀 (зелёный), пакеты OFFER возвращаются, пул 15/40

## Использование

```bash
# Скопируйте шаблон и замените содержимое
cp templates/report_dark_20260909.html my-report.html
# Отредактируйте секции под свои данные
# Откройте в браузере — анимации запустятся автоматически
```

## Лицензия
MIT

## 📬 Контакты

Вопросы? Пишите: **[allumaxmail@gmail.com](mailto:allumaxmail@gmail.com)**

---

<div align="center">

[![English](https://img.shields.io/badge/README-English-blue)](README.md)
[![Русский](https://img.shields.io/badge/README-Русский-red)](README.ru.md)
[![Oʻzbekcha](https://img.shields.io/badge/README-Oʻzbekcha-green)](README.uz.md)

</div>
