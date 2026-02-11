├── multiwindow_support: "teljes|részleges|nem"
├── galaxy_fold_optimized: "igen/nem" 
├── split_screen_rating: "1-10"
└── recommendation: "Install|Test|Skip"

{
  "objective": "Android multi-window app kompatibilitás elemzés",
  "persona": "Android fejlesztő, Foldable specialista",
  "context": {
    "devices": "Galaxy Fold6, OneUI 6.1+, Taskbar split screen",
    "focus": "multitasking, drag-drop, resizable windows"
  },
  "constraints": [
    "Play Store top app-ok priorizálása",
    "Foldable optimalizáció értékelése",
    "Split screen rating 1-10"
  ],
  "output_format": {
    "app_name": "App neve",
    "multiwindow_support": "teljes|részleges|nem",
    "galaxy_fold_optimized": "igen/nem",
    "split_screen_rating": "1-10",
    "play_store_rating": "szám",
    "recommendation": "Install|Test|Skip"
  }
}


## TESZT
ANDROID ADATOK: "Samsung OneUI 6.1 split screen, Taskbar multiwindow, keresek app-ot ami támogatja Galaxy Fold6 multi-window-t, Chrome, YouTube, Edge tesztelve"

A Galaxy Fold6 OneUI 6.1+ rendszerén a multi-window funkció (Taskbar, split screen) támogatása kulcsfontosságú a foldable multitaskinghoz, különösen drag-drop és resizable window funkcióknál. A Play Store top app-ok közül priorizálva elemzem a relevánsakat (Chrome, YouTube, Edge alapján, kiegészítve gyakori top app-okkal), foldable optimalizációval és split screen ratinggel. [reddit](https://www.reddit.com/r/GalaxyFold/comments/1lzth3s/can_i_watch_youtube_on_half_screen_fullscreened/)

## Top App-ok Elemzése

| app_name | multiwindow_support | galaxy_fold_optimized | split_screen_rating | play_store_rating | recommendation |
|----------|---------------------|-----------------------|---------------------|-------------------|---------------|
| YouTube | teljes | igen | 9 | 4.4 | Install  [reddit](https://www.reddit.com/r/GalaxyFold/comments/1lzth3s/can_i_watch_youtube_on_half_screen_fullscreened/) |
| Chrome | teljes | igen | 8 | 4.2 | Install  [youtube](https://www.youtube.com/watch?v=9txgsWGYFd0) |
| Microsoft Edge | teljes | részben | 7 | 4.5 | Test |
| Gmail | teljes | nem | 6 | 4.3 | Test |
| Google Keep | részleges | nem | 5 | 4.6 | Skip |
| Spotify | részleges | nem | 4 | 4.4 | Skip  [samsung](https://www.samsung.com/uk/support/mobile-devices/how-to-use-the-multi-window-function-in-android-pie/) |

## Részletes Értékelés
YouTube kiválóan működik split screenben FlexMode-dal, Labs beállítás után fullscreen videókkal Galaxy Fold6-on, ideális multitaskinghoz.  Chrome és Edge natívan támogatja a resizable window-kat Taskbarral, de Edge kevésbé optimalizált foldable hinge-re.  Gmail alap split screen-t kezel, de drag-drop gyenge; Keep és Spotify csak alap multi-window, nem resizable Fold6-on. [reddit](https://www.reddit.com/r/GalaxyFold/comments/1n1na5v/owned_a_fold_for_two_years_but_only_now_learned/)

## Fejlesztői Tanácsok
Foldable specialista szemszögből Jetpack WindowManager használatát javaslom app-jaidhoz, FoldingFeature-rel a hinge detektáláshoz.  Priorizáld Labs -> Multi Window engedélyezését, és teszteld Taskbar drag-drop-ot top app-okkal a teljes kompatibilitásért. [devblogs.microsoft](https://devblogs.microsoft.com/surface-duo/multi-window-foldable/)
