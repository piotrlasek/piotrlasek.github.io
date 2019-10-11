---
layout: page
title: Tworzenie GUI
permalink: /for-students/tgui
exclude: true
---

# Informacje

Zaliczenie:

* Obecność i praca na laboratorium zakończona prezentacją raportu.
* Kolokwium z treści wykładowych.

**Egzamin:**

* **23 stycznia 2017 r., godz. 8:00, sala 127.**
* [Materiały do egzaminu i kolokwium](tgui-test.html.pdf).

# Laboratorium

1. Propozycje projektów i analiza
 * Wybór typu projektu (Interfejs webowy, interfejs desktopowy, interfejs mobilny, inny).
 * Wybór konkretnego tematu.
 * Analiza. (a) Charakterystyka użytkowników (zebranie informacji od 3 użytkowników). (b) Określenie zadań związanych z projektem. Np. aplikacja powinna umożliwiać zamówienie taksówki, która znajduje się najbliżej. (c) Istotne elementy interfejsu (od strony technicznej). (d) Zależności pomiędzy komponentami. (e) Zdefiniowanie podstawowych elementów systemu w formie diagramu.
 * Strona internetowa projektu, która docelowo będzie stanowić końcowy raport dotyczący wykonanego projektu.

2. Projektowanie.
  * *Scenariusz*. Napisz scenariusz zachowania użytkownika, który uwzględnia zadania zdefiniowane w punkcie 1. Zadania w scenariuszu powinny być konkretne i odnosić się do wybranego typu interfejsu i komponentów wybranego projektu.
  * *Storyboard*. Wygeneruj trzy wstępne projekty interfejsu użytkownika. Wyjaśnij każdy z nich i załącz storyboard pokazujące jak interfejs działa. Storyboard powinien łączyć opis z odpowiednimi szkicami pokazując jak interfejs będzie się zmieniał zgodnie ze scenariuszem. Po dokonaniu takiej analizy powinieneś móc wskazać dobre i złe strony projektu interfejsu z punktu widzenia przyswajalności, przejrzystości, wydajności i odporności na błędy.
 + Nie wchodź zbytnio w szczegóły. Skup się na koncepcji modelu interfejsu i komunikacji z użytkownikiem oraz na prostocie. Poświęcanie zbyt dużo czasu na projektowanie szczegółowego wyglądu interfejsu na tym etapie jest bezcelowe - w kolejnej iteracji może się zdarzyć, że konieczne będą duże zmiany. Preferowane są rysunki odręczne. Po narysowaniu należy dołączyć je (np. robiąc zdjęcie) do strony - raportu.

3. Prototypowanie na papierze
  * Budowanie prototypu. Narysuj tło, menu, okienka dialogowe i inne potrzebne elementy interfejsu. Zdecyduj, jak zaimplementować dynamiczne części interfejsu. Nie musisz przygotowywać każdego możliwego ekranu. Naucz się tworzyć potrzebne okna “w biegu”.
  * Przygotuj briefing dla użytkowników. Przygotuj co najwyżej jedną stronę tekstu, który wyjaśni jakie jest zastosowanie Twojej aplikacji. Podaj potrzebne informacje potrzebne dla użytkownika testowego. Informacje powinny być krótkie, proste i przejrzyste. Pamiętaj, że briefing to nie podręcznik ani instrukcja użytkownika.
  * Zapisz zadania ze scenariusza na osobnych karteczkach. Scenariusz powinien uwzględniać przynajmniej 3 zadania. Zapisz je i przekaż testerom. Sformułuj je w postaci konkretnych zadań (np. “Kup mleko, pomidory i chleb”). Zadania powinny być krótkie (wykonanie jednego nie powinno zająć więcej niż 5 minut).
  * Wybierz 2-3 osoby i poproś je o to, aby przetestowały Twój interfejs.
  * Zapisz obserwacje. Jeśli wystąpiły jakieś problemy, wyciągnij wnioski i popraw swój prototyp.
  
4. Prototypowanie na komputerze
  Należy użyć komputerowego narzędzia do prototypowania interfejsu graficznego, np. [Pencil](http://pencil.evolus.vn/). 
  Prototyp stworzony na komputerze powinien charakteryzować się:
  * Dużą *wiernością* w wyglądzie. Za pomocą prototypu sprawdź jak rzeczywiście będzie wyglądać
    końcowa implementacja interfejsu. Rozłóż na ekranie poszczególne elementy w taki sposób
    jak przewidujesz, że będą rozłożone w docelowej aplikacji.
    Podejmij decyzje dotyczące kolorów, czcionek, wyrównania tekstu, ikon.
  * Dużą *wiernością* w odbiorze.
    Prototyp powinien w miarę dokładnie odpowiadać typowi interfejsu, jaki został
    wybrany (desktop, web, mobile).
  * Powinien *implementować* wszystkie funkcjonalności przewidziane przez opracowany
    wcześniej scenariusz. Nie powinien też wykraczać poza ten scenariusz.
  * Nie ma potrzeby implementowania backend'u na tym etapie.

5. Implementacja
  * Interfejs należy zaimplementoawć w technologii adekwatnej do wybranego typu interfejsu
    (desktop, web, mobile).
  * Nie ma potrzeby implementowania backend'u (np. dostęp do bazy danych, zapisywanie danych)
    aczkolwiek interfejs powinien prezentować przykładowe dane.
  * Interfejs powinien symulować operacje, które da się wykonać przy użyciu docelowego systemu.
    Przykładowo, jeśli system ma służyć do rejestracji pacjentów, osoba testująca powinna
    mieć możliwość testowego stworzenia i dodania przykładowej osoby. Jak wspomniano wcześniej,
    nie ma konieczności implementowania funkcji służących do dostępu do danych.
  
6. Testowanie
  * Poproś 3 osoby o wykonanie testów polegających na zrealizowaniu opracowanych wcześniej
    scenariuszy.
  * Zbierz od testerów komentarze.
  * Podsumuj zebrane informacje i wyciągnij wnioski dotyczące trzech podstawowych wymiarów
    użyteczności.
  * Czy projekt intefrejsu wymaga poprawek? Umotywuj prawidłowo swoją odpowiedź.


# Slajdy

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vQYfsVYcRhJLq7fVcJuAmommmwoa8wMp3Y_KdMRfih5OdwjYACNnTrQhV52htrk3Ownq45SCrbTwoF6/embed?start=false&loop=false&delayms=3000" frameborder="0" width="480" height="299" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

<iframe src="https://docs.google.com/presentation/d/18dfJPIu0ds870Y9fQtPkXnZrWvTptGvp4OYFU4TWQJ4/embed?start=false&loop=false&delayms=3000" frameborder="0" width="480" height="299" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

<iframe src="https://docs.google.com/presentation/d/1wcK2kLiyWAXcoUfOfp438rsT0zGmfPcHAEAxhBGE4KE/embed?start=false&loop=false&delayms=3000" frameborder="0" width="480" height="299" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>
