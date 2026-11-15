# Gem, set, Święta!

Świąteczna zabawa dla całej rodziny z tenisem w tle, przygotowana pod telefon.

Strona: https://wrobhu.github.io/swieta/

- intro z saniami Mikołaja, padający śnieg i zaśnieżony kort,
- odliczanie do Wigilii,
- konto to imię i jeden z 9 symboli świątecznych: to samo imię z tym samym symbolem na innym telefonie albo po wyczyszczeniu przeglądarki przywraca złote piłki i kupon, a cudze imię bez właściwego symbolu jest zablokowane,
- list Huberta do Mikołaja z podpisem i lista prezentów rozpakowywanych uderzeniem piłki,
- „Złote piłki Mikołaja”: każdy gość ma 7 piłek ukrytych w innych miejscach (z 22 możliwych), szukać można do 20 grudnia. Za 3 jest brązowy kupon, za 5 srebrny, za 7 złoty, każdy z kodem QR. Hubert skanuje kod i widzi numer prezentu do wręczenia,
- turniej na żywo: siedem mini-gier (m.in. Wieża z prezentów i Świąteczne memory) i gra bonusowa, wszyscy grają w tej samej chwili, a wejście jest przez sejf i znak turnieju.

Cała strona to jeden plik `index.html` bez zależności poza czcionkami Google, biblioteką do kodów QR i Firebase.

## Gra na żywo (Firebase)

Turniej, lista osób na stronie i panel Mikołaja działają przez Firebase (darmowy plan Spark wystarcza na kilkanaście osób naraz).

1. W konsoli Firebase włącz logowanie **Anonimowe** i utwórz **Realtime Database**.
2. W zakładce **Reguły** bazy wklej zawartość `firebase-rules.json` i wpisz swój 4-cyfrowy kod w miejsce `TU-WPISZ-4-CYFRY`. Kod sprawdza serwer, więc nie ma go w kodzie strony.
3. Obiekt `firebaseConfig` projektu jest w `index.html`, w `var FIREBASE_CONFIG`.
