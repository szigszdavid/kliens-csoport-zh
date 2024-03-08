# Kliensoldali webprogramozás csoportzh -- Progresszív fejlesztés

## Tudnivalók

A feladat beküldésével az alább leírtakat megértettnek és elfogadottnak tekintjük annak a nevében, aki a megoldást beküldte.

```txt
<Hallgató neve>
<Neptun kódja>
Ezt a megoldást a fent írt hallgató küldte be és készítette
a Kliensoldali webprogramozás kurzus csoport ZH-jához.
Kijelentem, hogy ez a megoldás a saját munkám. Nem másoltam vagy
használtam harmadik féltől származó megoldásokat. Nem továbbítottam
megoldást hallgatótársaimnak, és nem is tettem közzé. Az Eötvös Loránd
Tudományegyetem Hallgatói Követelményrendszere (ELTE szervezeti és
működési szabályzata, II. Kötet, 74/C. §) kimondja, hogy mindaddig,
amíg egy hallgató egy másik hallgató munkáját - vagy legalábbis annak
jelentős részét - saját munkájaként mutatja be, az fegyelmi vétségnek számít.
A fegyelmi vétség legsúlyosabb következménye a hallgató elbocsátása az egyetemről.
```

## 1. Képek késleltetett betöltése + háttérszín + folyamatsáv (10 pont)

Egy hosszú oldalon szeretnénk a képeket csak akkor megjeleníteni, amikor azok a képernyő területére beérnek, így minimalizálva az oldal betöltésekor elküldött HTTP kérések számát. A képeknél a kép forrása a `data-src` attribútumban van tárolva, innen kell megjelenítéskor az értékét az `src` attribútumba másolni.

- a\. (2 pont) Ha egy kép a megjelenített területre (viewportra) kerül, akkor a konzolra írjuk a kép `data-src` attribútumát!
- b\. (1 pont) Ebben az esetben másoljuk a `data-src` attribútum értékét az `src` tulajdonságába.
- c\. (1 pont) Ugyanekkor adjuk hozzá a `loaded` stílusosztályt is!
- d\. (1 pont) Legyen a megoldásod hatékony, azaz ha lehet, minél kevesebbszer meghívódó eseménnyel operáljon!
- e\. (1 pont) Ha elgördült az oldal 200px-nyit, akkor változtassuk meg az oldal háttérszínét egy tetszőleges színre.
- f\. (1 pont) Ügyelj arra, hogy a scroll esemény nagyon sokszor hívódik meg, ezért használhatod a lodash könyvtárbeli \_throttle függvényt!
  throttel elérése: <script src="https://cdn.jsdelivr.net/npm/lodash@4.17.21/lodash.min.js"></script>
- g\. (3 pont) Helyezz el egy olvasási folyamatsávot az oldal tetején. A gördítés mértéke szerint változzon 0 és 100% között a szélessége!

## 2. Leegyszerűsített torpedó játék

- a\. (0.5 pont) Delegálással kezeld a táblázatba klikkelést és írasd ki a klikkelt mező sor (element.parentNode.rowIndex) és oszlopszámát (element.cellIndex)
- b\. (0.5 pont) A klikkelt td tartalmát változtasd meg egy ❌-re
- c\. (0.5 pont) Abban az esetben, ha ott már van egy hajója az első játékosnak akkor a kattintás után ne változzon meg a tartalma
- d\. (1.5 pont) Abban az esetben, ha a klikkeléssel megegyező koordinátán az második játékosnak:
  - Van hajója, akkor az első játékos tábláján azon a helyen legyen ✔, a második játékosnak pedig ☠
  - Ha nincs hajója, akkor az első játékos tábláján azon a helyen legyen ❌, a második játékosnál nem változtatunk semmit
    Továbbá akkor helyes ez a feladat, ha abban az esetben, amikor saját hajóra kattintunk nem történik semmi.
- e\. (0.5 pont) Számoljuk, hányszor sikerült eltalálni, hogy hol van a második játékosnak hajója, mentsük el ezt az értéket egy változóba.
- f\. (1 pont) Programozottan adjunk hozzá mindkét playerContainer elemhez egy sort pl. span, amiben megjelenítjük az adott játékos aktuális pontját. Ehhez először készítsünk egy új span elemet, majd írjuk bele az kezdő pontot. Végül append-el adjuk hozzá az oldahoz.
  Tipp: Abban az esetben ha a querySelectorral a player1Container-t válaszottad ki, akkor azon könnyedén lehet használni az append-et. Viszont ha a table-t választottad, akkor előbb meg kell szerezni annak a parentNode-ját, ez lesz a player1Container és ehhez már lehet span-t appendálni. Nem kell semmilyen formázást alkalmazni!
- g\. (5.5 pont) Okosítsuk fel a második játékos pályáját is.
  Szabályok a feladathoz:
  - 1\. A feladat megoldásához muszáj valamilyen fajta egységbezárás használata (osztály vagy függvény).
  - 2\. Csak egy darab osztályt (vagy függvényt) lehet definiálni az egységbezárás eléréséhez, de természetesen majd kétszer kell azt példányosítani.
  - 3\. (1.5 pont)-ot ér, ha kattintás eseménykezelését kiszervezed egy függvénybe, pl. handleClick

### Tipp #1: Ha osztályba szervezitek a kódot ne feletkezetek el a this használatáról.

### Tipp #2: Az osztály konstruktora kapja meg mindkét táblázatot, majd példányosítsd kétszer az osztályt.
