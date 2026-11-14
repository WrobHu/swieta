# Gem, set, Święta!

Świąteczna, tenisowa lista życzeń do Mikołaja, przygotowana pod telefon.

Strona: https://wrobhu.github.io/swieta/

- padający śnieg, sanie Mikołaja i księżyc w kształcie piłki tenisowej,
- odliczanie do Wigilii,
- lista prezentów rozpakowywanych uderzeniem piłki,
- zabawa „Złote piłki Mikołaja”: 7 ukrytych piłek, srebrny kupon za 3, złoty za 7, kupon z kodem QR do pokazania w Święta.

Cała strona to jeden plik `index.html` bez zależności poza czcionkami Google i biblioteką do kodów QR.

## Gra na żywo (Firebase)

Ranking, lista osób na stronie i raport prób złamania kodu działają przez Firebase (darmowy plan Spark).

1. W konsoli Firebase włącz logowanie **Anonimowe** i utwórz **Realtime Database**.
2. W zakładce **Reguły** bazy wklej zawartość `firebase-rules.json` i wpisz swój tajny kod w miejsce `TU-WPISZ-SWOJ-TAJNY-KOD`. Kod jest sprawdzany przez serwer, więc nie ma go w kodzie strony.
3. Wklej obiekt `firebaseConfig` w `index.html`, w miejscu `var FIREBASE_CONFIG = null;`.
