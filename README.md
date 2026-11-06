Poweramp Equalizer — AutoEq Presets Collection
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

FOLDER STRUCTURE
----------------
parametric_eq/   8,850 files - AutoEq "parametric_eq.txt" format (REW style)
graphic_eq/      8,853 files - AutoEq "GraphicEQ" format
index.csv        index of all presets (see columns below)
all_presets.json complete structured dump of every preset
auto_eq.db       the original, untouched SQLite database from the APK

Files are named:  "<Model> [<Measurement source> <form>].txt"
e.g. "Sennheiser HD 650 [Oratory1990 over-ear].txt"

PREAMP NOTE
------------
The Poweramp database stores preamp = 0 for every AutoEq preset (the app
relies on its own DSP headroom). For safe use in other software:

  - parametric_eq/*.txt files include a "Preamp" line computed the
    standard AutoEq way (negative of the preset's maximum boost, from
    the actual combined filter-bank response). It only attenuates -
    tonality is unchanged, digital clipping is avoided.
  - GraphicEQ files cannot carry preamp; column
    "graphic_suggested_preamp_db" in index.csv holds the equivalent
    value (negative of the loudest band) if your app supports preamp.

