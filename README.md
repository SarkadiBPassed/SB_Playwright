**Intelligens TimeSheet (Munkaidő-nyilvántartás) kitöltés**


**Üzleti kontextus:** A munkavállalóknak rendszeresen rögzíteniük kell a projekten töltött munkaidejüket. A rendszerben minden felhasználóhoz tartozik egy alapértelmezett napi munkaidő (pl. 8 óra, 6 óra vagy 4 óra), és a könyvelést csak egy megadott időszakra (pl. egy adott hétre vagy hónapra) kell
elvégezni.

**Feladat leírása:** Ez egy automatizált teszt, amely bejelentkezik egy adott felhasználóval , és kitölti a TimeSheetjét egy paraméterben megadott időszakra (startDate – endDate) és projektre.

**Műszaki leírás:**

* **Dinamikus munkaidő-lekérdezés:** A teszt először a felületről kiolvassa (pl. a felhasználó profiljából vagy munkaszerződés adataiból) a hozzá rendelt napi munkaidőt, és ezzel az értékkel dolgozik.
* **Paraméterezhető időszak:** Az időszakot (mettől - meddig) környezeti változóból vagy konfigurációs fájlból olvassa be.
* **Dátumkezelés:** Csak a munkanapokra (hétfőtől péntekig) rögzít munkaidőt a megadott intervallumon belül (hétvégéket kihagyja, kivéve, ha a felület
  maga is csak a munkanapokat engedi).
* **Ellenőrzés (Assertion):** A mentés után ellenőrizi, hogy a rögzített órák összege a felületen megegyezik-e a (munkanapok száma × napi
  munkaidő) értékkel, és a státusz megfelelően frissült-e.
