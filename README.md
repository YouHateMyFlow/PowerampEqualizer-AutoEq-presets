Poweramp Equalizer AutoEq Presets
===============================================
Extracted from: Poweramp Equalizer build-1021-bundle-play
                (com.maxmpz.equalizer, versionCode 1021004, Android 9.0+)
Source inside APK: assets/auto_eq.db (SQLite, table eq_presets)

WHAT THIS IS
------------
Poweramp Equalizer ships with the complete AutoEq community measurement
database (the data behind autoeq.app): correction presets for headphones
and IEMs measured by 29 different sources / measurement rigs.

I've personally found the AutoEq GitHub and website to give presets
inconsistently and of poor quality, yet for some reason, Poweramp's
database is consistently great from my experience.

Go support the wonderful Poweramp and Poweramp Equalizer apps!

PREAMP NOTE
------------
The Poweramp database stores preamp = 0 for every AutoEq preset (the app
relies on its own DSP headroom). For safe use in other software:

  - Parametric EQ files include a "Preamp" line computed the
    standard AutoEq way (negative of the preset's maximum boost, from
    the actual combined filter-bank response).
  - GraphicEQ files cannot carry preamp; column
    "graphic_suggested_preamp_db" in index.csv holds the equivalent
    value (negative of the loudest band) if your app supports preamp.
