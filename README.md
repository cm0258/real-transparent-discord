# transparent-discord

Siyah, yarı saydam Discord teması — duvar kağıdın hafif görünür, yazılar ve resimler net kalır. Sürümden bağımsız seçiciler kullanır (hash kovalaman gerekmez), uzak `@import` içermez.

## Önizleme

- Uygulama zemini: siyah %70 opak (`rgba(0,0,0,0.3)`)
- Menüler + ayarlar: hafif karartma + 6px blur
- Profil renkleri, rozetler, sunucu resimleri korunur

## Kurulum (Vencord)

1. Discord Ayarlar → Vencord → **QuickCSS**'i aç
2. `quickCss.css` içeriğini yapıştır
3. `Ctrl+R` ile Discord'u yenile

## Gerekenler

- **Vencord** kurulu olmalı
- Ayarlar → Vencord → **Transparent** açık olmalı (şeffaf pencere)
- Linux'ta pencere saydamlığı için Discord'u şu bayrakla başlat:
  `discord --enable-transparent-visuals`

## Özelleştirme

| Ne | Nerede |
|---|---|
| Zemin opaklığı | `.appMount__51fd7` → `rgba(0,0,0,0.3)` |
| Menü/ayar karartması | `[role="menu"], [role="dialog"]` → `rgba(0,0,0,0.5)` |
| Blur miktarı | `backdrop-filter: blur(6px)` |

## Nasıl çalışıyor?

- Tek kural tüm arka planları saydam yapar; profil (`userProfile`), başlık (`banner`) ve resimler istisnadır
- Menü/ayar seçicileri `role` özniteliğine dayanır — Discord sınıf isimlerini değiştirse bile çalışmaya devam eder

## Lisans

MIT
