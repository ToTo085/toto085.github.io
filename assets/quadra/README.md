# Quadra — Brand Asset Pack
**Versione 1.0 · Maggio 2026**

Identità visiva per *Quadra*, app di finanza personale.

## Sistema
- **Nome:** Quadra
- **Dominio:** quadra.gioia.ovh
- **Claim:** *I conti quadrano.*
- **Mark:** Coin v3 — tre cerchi concentrici (bordo zigrinato di moneta) + coda verticale della Q che esce sotto l'anello
- **Tipografia:** Cormorant Garamond (display) · Inter (UI) · JetBrains Mono (numeri)
- **Palette:** Petrolio #06100F · Card #162C32 · Oro #D4AF37 · Avorio #F4EEDD

## Struttura
```
assets/quadra/
├── svg/                        # Sorgenti vettoriali editabili
│   ├── icon-coin.svg           # Mark da solo (linea, sfondo trasparente)
│   ├── icon-coin-solid.svg     # Versione piena (favicon, featured)
│   ├── icon-coin-tiny.svg      # Variante per dimensioni <48 px
│   ├── icon-app.svg            # Icona app 1024 con sfondo petrolio
│   ├── wordmark.svg            # Wordmark "Quadra" oro
│   ├── wordmark-ivory.svg      # Wordmark avorio (per sfondi oro)
│   ├── lockup-horizontal.svg   # Mark + wordmark in riga
│   ├── lockup-stacked.svg      # Lockup verticale con claim
│   └── favicon.svg             # Favicon ottimizzato 32×32
│
├── ios/
│   └── AppIcon.appiconset/     # Da trascinare in Xcode → Assets.xcassets
│       ├── Contents.json
│       ├── icon-1024.png       # App Store master
│       ├── icon-180.png        # iPhone @3x
│       ├── icon-167.png        # iPad Pro
│       ├── icon-152.png        # iPad
│       ├── icon-120.png        # iPhone @2x
│       ├── icon-87.png         # Settings @3x
│       ├── icon-80.png         # Spotlight
│       ├── icon-76.png         # iPad legacy
│       ├── icon-60.png         # Notifiche @3x
│       ├── icon-58.png         # Settings @2x
│       └── icon-40.png         # Notifiche @2x
│
├── android/
│   ├── mipmap-anydpi-v26/      # Icona adattiva (Android 8+)
│   │   ├── ic_launcher.xml
│   │   ├── ic_launcher_round.xml
│   │   ├── ic_launcher_foreground.png  # 432×432, safe zone centrale
│   │   └── ic_launcher_background.png  # 432×432, tinta unita
│   ├── mipmap-xxxhdpi/         # 192 px — legacy
│   ├── mipmap-xxhdpi/          # 144 px
│   ├── mipmap-xhdpi/           # 96 px
│   ├── mipmap-hdpi/            # 72 px
│   ├── mipmap-mdpi/            # 48 px
│   ├── ic_notification.png     # 96×96 bianco monocromo
│   └── play-store-512.png      # Listing Play Store
│
├── web/
│   ├── favicon.svg             # Vettoriale (default per browser moderni)
│   ├── favicon-16.png · 32.png · 48.png
│   ├── apple-touch-icon.png    # 180×180 per iOS Safari
│   ├── android-chrome-192.png · 512.png
│   └── site.webmanifest        # PWA manifest pronto all'uso
│
└── preview/                    # PNG ad alta risoluzione per slide e press
    ├── mark-256.png · 512.png · 1024.png  (sfondo trasparente)
    └── coin-solid-1024.png
```

## Installazione

### iOS (Xcode)
1. Trascina la cartella `ios/AppIcon.appiconset` dentro `Assets.xcassets` del progetto.
2. In `Info.plist` imposta `CFBundleIconName = AppIcon`.
3. Pulito + ricompila.

### Android (Studio)
1. Copia il contenuto di `android/` dentro `app/src/main/res/`.
2. In `AndroidManifest.xml` verifica `android:icon="@mipmap/ic_launcher"` e `android:roundIcon="@mipmap/ic_launcher_round"`.
3. Per le notifiche: `R.drawable.ic_notification` (importa il PNG come drawable).

### Web (HTML head)
```html
<link rel="icon" type="image/svg+xml" href="/favicon.svg">
<link rel="icon" type="image/png" sizes="32x32" href="/favicon-32.png">
<link rel="icon" type="image/png" sizes="16x16" href="/favicon-16.png">
<link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png">
<link rel="manifest" href="/site.webmanifest">
<meta name="theme-color" content="#162C32">
```

## Note sul mark
Il **Coin** ha due strati di anelli (faint outer + faint inner, attorno al ring centrale spesso) che funzionano sopra i 48 px ma scompaiono sotto. Per i tiny size (favicon-16, notifica, watch complication) usa `icon-coin-tiny.svg` o, in alternativa, ridisegna il mark con solo cerchio centrale + slash.

Lo **Slash** è la firma condivisa con il logo personale **Antonio Gioia** — non è decorazione, è un richiamo intenzionale al *mother brand*.

## Tipografia (font da licenziare/embeddare)
- **Cormorant Garamond** — [Google Fonts](https://fonts.google.com/specimen/Cormorant+Garamond), Open Font License, gratis.
- **Inter** — [Google Fonts](https://fonts.google.com/specimen/Inter), Open Font License, gratis.
- **JetBrains Mono** — [JetBrains](https://www.jetbrains.com/lp/mono/), Apache 2.0, gratis.

Tutte usabili in app commerciali senza royalty.
