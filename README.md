# Boğaziçi University Computational Social Science Society

Quarto ile kurulmuş statik site. GitHub Pages üzerinde yayınlanıyor.

## Kurulum (bir kereye mahsus)

1. [Quarto'yu kur](https://quarto.org/docs/get-started/). Kontrol: `quarto --version`
2. `_quarto.yml` içindeki `ORGANIZATION` yazan yerleri gerçek GitHub hesabı/organizasyon adıyla değiştir.
3. `contact.qmd` içindeki e-posta adresini gerçek adresle değiştir.
4. Fotoğrafları `images/people/` klasörüne koy (kare kırpılmış, ~500x500).

## Yerelde çalışma

```bash
quarto preview
```

Tarayıcı açılır, her kaydetmede yenilenir. Durdurmak için control-C.

## Yayınlama

```bash
quarto publish gh-pages
```

## Yeni etkinlik eklemek

`events/` klasörüne yeni bir `.qmd` dosyası ekle. Başlığı şu formatta olmalı:

```
---
title: "Etkinlik başlığı"
description: "Bir cümlelik açıklama."
date: 2026-11-12
categories: [workshop, network analysis]
---
```

Etkinlik otomatik olarak Events sayfasında, tarihe göre sıralanmış şekilde görünür.
Dosya adı önemli değil ama `2026-11-konu.qmd` gibi olması arşivi düzenli tutar.

## Kişi eklemek

`people.qmd` içindeki blokları kopyalayıp düzenle. Fotoğraf yoksa
`images/people/placeholder.jpg` kalabilir.

## Yapı

| Dosya | İşlevi |
|---|---|
| `_quarto.yml` | Site başlığı, navigasyon, tema |
| `custom.scss` | Tüm görsel tasarım — renkler, tipografi, düzen |
| `head.html` | Google Fonts yükleyici |
| `index.qmd` | Ana sayfa (hero'daki ağ grafiği burada gömülü) |
| `events.qmd` + `events/` | Etkinlik listesi; klasördeki her `.qmd` bir girdi |
| `_site/` | Üretilen çıktı — düzenleme, commit'leme |

## Tasarımı değiştirmek

`custom.scss` dosyasının en üstündeki değişkenler en hızlı kaldıraç:

- `$navy` — kurumsal lacivert
- `$teal` — vurgu rengi
- `$paper` — sayfa zemini
- `$font-size-root` — genel yazı boyutu
