# CodeM Versions

Scriptlerin guncel surum ve changelog kayitlari. Musterilerin sunucusundaki
`versionchecker.lua` bu repoyu okur.

Bu repoda kod yoktur, sadece veri vardir. Klasor adlari, dosya adlari ve
asagidaki format musteri sunucularindaki scriptler tarafindan okundugu icin
bunlari degistirmek dagitilmis butun kurulumlari etkiler. `versionchecker.lua`
bu repoda bulunmaz; okuma ve karsilastirma mantigi her scriptin kendi
icindedir. Repo'nun varsayilan dali `main`.

## Yapi

    <script-adi>/
      version.json    guncel surum
      changelog.md    surum notlari

Klasor adi, script tarafindaki `VersionChecker.key` degeriyle birebir ayni
olmalidir. Bir klasorun adini degistirmek, o scripti kullanan musterilerde
surum kontrolunu bozar.

## Kayitli scriptler

    codem-admin                  codem-motelcreator
    codem-camera                 codem-pettycrimes
    codem-carservice             codem-phone
    codem-clothing               codem-racing
    codem-dispatchv2             codem-radiov2
    codem-dynamicweather         codem-supreme-hud
    codem-emotemenu              codem-supreme-market
    codem-fishing-simulator      codem-supreme-multicharacter
    codem-fuel                   codem-supreme-settings
    codem-gps                    codem-supreme-uipack
    codem-inventoryv2            codem-tv
    codem-mdtv2
    codem-mechanicv2

Guncel surumler her klasorun `version.json` dosyasindadir.

## Yeni surum cikarirken

1. Script'in `fxmanifest.lua` dosyasinda `version` degerini artir
2. Buradaki `<script-adi>/version.json` icindeki `version` degerini ayni yap
3. `<script-adi>/changelog.md` dosyasinin en ustune yeni blok ekle

Commit mesaji icin ornek: `codem-mdtv2 2.0.9`.

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

Notlar:

- Anahtarlarin sirasi onemli degil (gecerli JSON olmasi yeterli). Bazi
  dosyalarda `critical` ve `message` once yaziliyor.
- Surum formati scriptten scripte farkli: `codem-phone` iki parca
  (`3.20`), `codem-inventoryv2` uc parca (`2.49.0`) kullaniyor. Karsilastirma
  mantigi `versionchecker.lua` icinde oldugu icin bir scriptin mevcut
  formatini degistirme; her zaman `fxmanifest.lua` ile ayni yaz.
- Su an hicbir scriptte `critical: true` veya dolu bir `message` yok.

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

### "Changed files" bolumu

Cogu blokta maddelerden sonra, hangi dosyalarin degistigini listeleyen bir
`### Changed files` alt basligi var:

    ## 1.0.3 - 2026-11-06

    - Fix: TV picture flickering on stock TV models

    ### Changed files

    fxmanifest.lua: version 1.0.3
    config/config.lua: Config.NowPlaying

Bu bolumdeki satirlar `- ` ile baslamaz, yani yukaridaki kurala gore madde
sayilmazlar. Satirlarin `- ` ile baslamamasina dikkat et. Bu bolumun musteri
konsolunda nasil gorundugu `versionchecker.lua` icinde belirlenir ve buradan
dogrulanamaz.

## Kontrol listesi

Yayinlamadan once:

- `version.json` icindeki `version` ile `changelog.md` icindeki en ustteki
  `## ` basligindaki surum ayni mi
- Ikisi de script'in `fxmanifest.lua` dosyasindaki `version` ile ayni mi
- `version.json` gecerli JSON mi (sonda virgul yok, cift tirnak)

Mevcut durumda dikkat edilmesi gerekenler:

- `codem-carservice/changelog.md` bos (sadece bir satir sonu). `version.json`
  `1.0.1` diyor ama bu surum icin not yok.
- `codem-dynamicweather/changelog.md` icindeki `## 1.2` basliginda tarih yok.
  Tarih opsiyonel oldugu icin bu kurala uygun.
