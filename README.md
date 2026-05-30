# Yabay Zeka

Türkçe metinlerden yapay zeka yazım kalıplarını temizleyen bir skill.

## Bu nedir?

Yapay zeka metinlerinin kalıpları vardır: öngörülebilir ifadeler, bürokratik ekler, dolgu kelimeler, gizlenen özne. Bu skill, Claude'a (veya herhangi bir LLM'e) bu kalıpları **Türkçede** yakalayıp temizlemeyi öğretir.

Bu, açık kaynak [Stop Slop](https://github.com/hardikpandya/stop-slop) skill'inin (MIT) Türkçe uyarlamasıdır. Çeviri değil, yeniden tasarım: İngilizcedeki AI belirtilerinin çoğu (em dash, "-ly" zarfları, Wh- ile başlama) Türkçeye oturmaz. Türkçenin kendi kalıpları vardır — `-mektedir/-maktadır` ekleri, gereksiz `-dir` ek-fiili, "söz konusu / bağlamında / noktasında" dolguları, "Gelin yakından bakalım" açılışları.

## Yapı

```
yabay-zeka/
├── SKILL.md              # Çekirdek talimatlar
├── referanslar/
│   ├── ifadeler.md       # Atılacak kelime ve kalıplar
│   ├── yapilar.md        # Kaçınılacak yapısal kalıplar
│   └── ornekler.md       # Öncesi/sonrası dönüşümler
├── README.md
├── CHANGELOG.md
└── LICENSE
```

## Hızlı başlangıç

**Claude Code:** Bu klasörü skill olarak ekleyin.

**Claude Projects:** `SKILL.md` ve referans dosyalarını proje bilgisine yükleyin.

**Özel talimatlar:** `SKILL.md`'deki çekirdek kuralları kopyalayın.

**API çağrıları:** `SKILL.md`'yi sistem isteminize ekleyin. Referans dosyaları gerektiğinde yüklenir.

## Hedef üslup

**Resmi ama temiz.** "Siz" dili ve saygı tonu korunur. Atılan şey resmiyet değil, **şişkinliktir**: bürokratik ekler, ek-fiil yığını, dolgu kalıpları, gizlenen özne.

## Neyi yakalar?

**Yasaklı kelime ve kalıplar** — Boğaz temizleme açılışları, plaza/karışık jargon, gereksiz zarflar, meta-yorum, **resmi şişkinlik ekleri** (`-mektedir`, `-dir`), **dolgu isim ve kalıplar** (söz konusu, bağlamında). Bkz. `referanslar/ifadeler.md`.

**Yapısal klişeler** — İkili karşıtlık, olumsuz listeleme, dramatik parçalama, sahte özne, uzaktan anlatıcı, **edilgen/kişisiz çatı**. Bkz. `referanslar/yapilar.md`.

**Türkçeye özgü kurallar** — Wh- yerine "Gelin/Peki/Şöyle ki" açılış takıntıları, sade zaman tercihi, uzun çizginin yalnızca diyalogda meşru olması.

## Puanlama

Her boyutu 1-10 arası puanlayın:

| Boyut | Soru |
|-------|------|
| Doğrudanlık | İfade mi, duyuru mu? |
| Ritim | Çeşitli mi, metronom gibi mi? |
| Güven | Okurun zekâsına güveniyor mu? |
| Doğallık | İnsan eli değmiş gibi mi? Resmi ama şişkin değil mi? |
| Yoğunluk | Kesilecek bir şey var mı? |

35/50 altı: revize edin.

## Yazar

[Ömer Doğan](https://omerdogan.dev/)

[Stop Slop](https://github.com/hardikpandya/stop-slop) (MIT) temel alınarak hazırlanmıştır.

## Lisans

MIT. Özgürce kullanın, geniş paylaşın.
