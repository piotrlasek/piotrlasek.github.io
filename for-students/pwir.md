---
layout: page
title: Programowanie współbieżne i rozproszone
permalink: /for-students/pwir
exclude: true
---

Edycja: **Zima 2019**<br>
Ostatnia aktualizacja: **15 stycznia 2020**

## Aktualności

* Termin kolokwium zostanie podany wkrótce.

<br>

## Wykłady

| Wykład 1 | Wykład 2 |
|----------|----------|
|<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vTs_LyEJOlezwI2TZLnFLaaI6fI1mjOjad-_VkHzAsDGo6xa-ltaCv0xP8TqbAaAlgSJD_x1rnIqDM3/embed?start=false&loop=false&delayms=3000" frameborder="0" width="400" height="250" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>|<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vTs_LyEJOlezwI2TZLnFLaaI6fI1mjOjad-_VkHzAsDGo6xa-ltaCv0xP8TqbAaAlgSJD_x1rnIqDM3/embed?start=false&loop=false&delayms=3000" frameborder="0" width="400" height="250" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>|

<br>

## Zasady zaliczenia laboratorium

Zaliczenie laboratorium odbywa się na podstawie zaliczenia czterech
indywidualnych mini-projektów. Do zaliczenia laboratorium wymagane
jest pozytywne zaliczenie wszystkich projektów. Każdy projekt składa
się z następujących elementów:

1. Implementacja zadania projektowego.
2. Wykonanie dokumentacji zadania w skład której muszą wchodzić:
   * Opis treści zadania.
   * Wyjaśnienie sposobu wykonania zadania.
   * Opis implementacji (np. wykorzystanych klas lub bibliotek).
   * Dyskusja wykonanych eksperymentów potwierdzających (lub nie)
     poprawność implementacji.
3. Obrona projektu w formie pytań dotyczących projektu. Przykładowe
   pytania podane są poniżej.

## Tematy zadań projektowych

* Preferowana technologia implementacji: *Język Java*.
* Dokumentacja do pakietu **java.util.concurrent** w postaci tutoriala dostępna jest [tutaj](https://docs.oracle.com/javase/tutorial/essential/concurrency/index.html).

1. Implementacja *Algorytmu Petersona*.
   * Celem zadania jest zaimplementowanie i przebadanie algorytmu
         Petersona.
   * Dokumentacja
    * [Wikipedia](https://pl.wikipedia.org/wiki/Algorytm_Petersona)
    * Slajdy do wykładu
2. Symulacja problemu producentów i konsumentów przy użyciu klasy *BlockingQueue*.
   * Zadanie polega na zaimplementowaniu i przebadaniu klasycznego
       problemu producentów i konsumentów przy użyciu klasy z pakietu
       java.util.concurrent o nazwie *BlockingQueue*. Po zaimplementowaniu
       należy sprawdzić poprawność implementacji.
   * [Dokumentacja](https://docs.oracle.com/javase/7/docs/api/java/util/concurrent/BlockingQueue.html)
3. Symulacja gaszenia pożaru przy użyciu klasy *Exchchanger*.
   * Wyobraźmy sobie następującą scenę. Po prawej stronie widzimy
       palący się budynek. Po lewej stronie znajduje studnia. Pomiędzy
       budynkiem i studnią znajduje się *k* osób, które będą gasić
       pożar. Gaszenie pożaru polega na przekazywaniu wiader
       napełnionych wodą od osoby, która znajduje się najbliżej studni
       do osoby, która znajduje się przy palącym się budynku. Osoba
       przy studni odpowiedzialna jest za napełnianie wiader,
       natomiast osoba przy budynku za ich opróżnianie. Należy przyjąć
       następujące założenia: liczba wiader jest równa liczbie osób,
       liczba obiektów *Exchanger* jest o 1 mniejsza od liczby osób.
   * [Dokumentacja](https://docs.oracle.com/javase/7/docs/api/java/util/concurrent/Exchanger.html)
   * [Przykładowa implementacja](https://github.com/piotrlasek/exchanger-demo)
4. Symulacja dworca autobusowego (lub lotniska) przy użyciu funkcji języja Java takich jak: notify / notifyAll / wait.
    * Przystanek, na którym gromadzą się pasażerowie pełni rolę
      obiektu za pomocą którego pasażerowie będą *synchronizować* się
      z autobusem. Każdy pasażer, dochodząc do przystanku, wywołuje na
      nim funkcję *wait* i zaczyna czekać na autobus. Autobus
      natomiast, jako odrębny wątek, po dojechaniu do przystanku,
      *wybudza* pasażerów za pomocą wywołania na przystanku funkcji
      *notifyAll*. 
    * [Guarded blocks](https://docs.oracle.com/javase/tutorial/essential/concurrency/guardmeth.html)
    * [Przykładowa implementacja](https://github.com/piotrlasek/bus-stop)

## Przykładowe pytania pomocne w zaliczaniu zadań projektowych

1. Algorytm Petersona.
   * Czym charakteryzuje się algorytm Petersona?
   * Wyjaśnić negatywne cechy algorytmu Petersona.
   * W którym momencie następuje zamiana procesów w sekcji krytycznej?
   * Wskazać i wyjaśnić w którym miejscu znajduje się *sekcja
     krytyczna*.
   * Dlaczego dwa procesy nie mogą jednocześnie znaleźć się w sekcji
     krytycznej?
2. *BlockingQueue*.
   * Co stanie się w przypadku kiedy producent wyprodukuje za dużo
       obiektów?
   * Co stanie się w przypadku kiedy konsument będzie próbował
       odbierać obiekty z pustego bufora?
   * Co się stanie jeśli producent będzie produkował zdecydowanie więcej
       obiektów niż konsument będzie konsumował.
3. Symulacja gaszenia pożaru.
   * Jaki wpływ na strażaków będzie miała niedyspozycja (niemożność
     przekazania wiadra w jedną lub drugą stronę) jednego z
     gaszących?
   * W jaki sposób należy zainicjować zmienne *Bucket*?
   * Co się stanie w sytuacji gdy wszystkie wiadra będą na początku
     puste?
   * Czy w przypadku wyschnięcia studni gaszący nadal będą przekazywać
     sobie wiadra?
4. Symulacja dworca / lotniska.
   * Co stanie się z pasażerami jeśli autobus nigdy nie przyjedzie?
   * Co stanie się jeśli autobus przyjedzie, ale na przystanku nie
     będzie pasażerów?
   * Co się stanie jeśli zamiast funkcji *notifyAll* wykorzysta się
     funkcję *notify*?


<!--
1. Obecność na laboratorium.
2. Implementacja i prezentacja mini-projektów.
3. Kolokwia wykładowe.
   * Terminy kolokwiów:
     * 30 listopada 2016 r. 
       * [Wyniki z pierwszego kolokwium](pwir-wyniki-2016.pdf) (do wglądu w godzinach konsultacji).
     * 18 stycznia 2016 r.
   * Materiały do przygotowania do kolokwium - dostępne wkrótce.
4. **Egzamin**.
   * **Termin zerowy:**
     * 20 stycznia 2017 r., sala 243, godz. 11:30.
   * Pierwszy termin:
     * 23 stycznia 2017 r., sala 243, godz. 9:00.
   * **Materiały do przygotowania do egzaminu i [kolokwium](pwir-kolokwium-2.pdf)**.
-->
