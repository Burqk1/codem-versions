# CodeM Versions

Scriptlerin guncel surum ve changelog kayitlari. Musterilerin sunucusundaki
`versionchecker.lua` bu repoyu okur.

## Yapi

    <script-adi>/
      version.json    guncel surum
      changelog.md    surum notlari

## Yeni surum cikarirken

1. Script'in `fxmanifest.lua` dosyasinda `version` degerini artir
2. Buradaki `<script-adi>/version.json` icindeki `version` degerini ayni yap
3. `<script-adi>/changelog.md` dosyasinin en ustune yeni blok ekle

## Yeni script eklerken

Yeni bir klasor ac, icine `version.json` ve `changelog.md` koy. Script tarafinda
`versionchecker.lua` icindeki `VersionChecker.key` degerini klasor adiyla ayni yap.

## version.json

    {
        "version": "1.4",
        "critical": false,
        "message": ""
    }

- `version`   : zorunlu, `fxmanifest.lua` ile ayni olmali
- `critical`  : true ise konsolda "KRITIK GUNCELLEME" yazar
- `message`   : doldurulursa changelog'un ustunde tek satir gorunur

## changelog.md

    ## 1.4 - 2026-09-10
    - Yeni CCTV kayit sistemi
    - Warrant sure ayari duzeltildi

    ## 1.3 - 2026-09-02
    - Overview istatistik ekrani

- Baslik: `## <surum> - <tarih>` (tarih opsiyonel)
- Maddeler: `- ` ile baslayan satirlar
- En yeni surum en ustte
- Musteri sadece kendi surumunden yeni olanlari gorur
