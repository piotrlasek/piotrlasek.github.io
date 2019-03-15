---
layout: page
title: Propozycje tematów prac inżynierskich na semestr letni 2017
permalink: /for-students/topics2017
exclude: true
---

Ostatnia aktualizacja: 13 marca 2019 r.


## Interaktywna wizualizacja i eksploracja danych

 1. Analiza i implementacja algorytmu k-średnich wspomagana strukturą
    pi-cube.
 2. Eksperymenty i implementacja interaktywnych metod dostępu 
    danych przy użyciu struktur hierarchicznych.
 3. Implementacja i testy nowej metody grupowania gęstościowego
    opartego o algorytm DBSCAN i granularną strukturę pi-cube.
 4. Implementacja i testy nowej metody grupowania gęstościowego
    opartego o algorytm NBC i granularną strukturę pi-cube.
 5. Projekt i implementacja webowego modułu interaktywnej wizualizacji
    dużych zbiorów danych na przykładzie zbioru Checkins.
 6. Projekt i implementacja webowego modułu interaktywnej wizualizacji
    dużych zbiorów danych na przykładzie zbioru Checkins.
 7. Projekt i implementacja modułu do testowania wydajności
    hiearchicznych struktur danych.
 8. Grupowanie przybliżone w oparciu o hierarchiczną strukturę danych
    - implementacja i analiza wybranych algorytmów.
 9. Grupowanie z ograniczeniami z wykorzystaniem sieci neuronowych do
    wyznaczania odległości pomiędzy obiektami.
10. Implementacja i analiza algorytmu DBSCAN przy użyciu platformy MADlib.
11. Implementacja i analiza algorytmu NBC przy użyciu platformy
    MADlib.





## Interaktywna wizualizacja i eksploracja danych

W kontekście eksploracji danych, słowo interaktywny może
odzwierciedlać jak wygląda, a w zasadzie jak powinna przebiegać praca
analityków danych. W 1996 Shneiderman sformułował sformułował swego
rodzaju metaforę opisującą proces analizy danych, tzw. mantrę
(Shneiderman, 1996), do której często odwołują się specjaliści jeśli
chcą wyjaśnić pojęcie interaktywnej eksploracji lub wizualizacji
danych. Wspomniana matra brzmiała: *Overview first, zoom and filter,
then details on demand*. Zgodnie z nią przykładowy interaktywny proces
analizy danych może wyglądać następująco: Analityk zadaje do systemu
zapytanie (ang. *analytical task*), oczekuje na odpowiedź, a następnie ją
analizuje, czyli stara się ją zrozumieć i ocenić. Jeśli na podstawie
odpowiedzi systemu nie jest w stanie wyciągnąć wartościowych dla
siebie wniosków, wówczas zmienia parametry zapytania i powtarza cały
proces. W przypadku kiedy czas odpowiedzi jest duży - powiedzmy
powyżej pięciu sekund - wówczas, taki proces, zgodnie ze standardami
HCI (*human-computer interaction*), staje się dla użytkownika
uciążliwy. W takiej sytuacji, nie możemy stwierdzić, że proces
analizy, czy eksploracji danych jest interaktywny. Ma to szczególne
istotne znaczenie kiedy zbiór danych jest duży. Jest to również powód
dla którego obecne metody eksploracji dużych danych stają się
niewystarczające. Operując na dużej liczbie obiektów, analityk nie
jest po prostu w stanie uzyskać odpowiedzi o systemu w krótkim czasie.
Niemniej jednak, zakładając, że użytkownika nie zawsze interesuje
*dokładny* wynik analizy (co w wielu przypadkach jest prawdą), wydaje
się, że odpowiedzią na opisany tutaj problem może być projektowanie
algorytmów w taki sposób, aby użytkownik mógł otrzymywać właśnie
przybliżoną odpowiedź w zadanym przez niego czasie.  Przykładowym
rozwiązaniem, które wykorzystuje ten pomysł jest prototypowa baza
danych BlinkDB (Agrawal, 2013), która pozwala użytkownikowi zadawać
zapytania specyfikując oczekiwany czas uzyskania wyniku oraz jego
zakładaną jakość.

Biorąc pod uwagę powyższy komentarz dotyczący eksploracji i
wizualizacji danych w kontekście projektowania i budowania systemów
działających w sposób interaktywny, proponujemy kilka
poniższych tematów prac inżynierskich.
Ich elementem wspólnym jest wykorzystanie specjalnej struktury
(pi-cube)
umożliwiającej dostęp do danych o zadanym stopniu granularności co
pozwala na redukcję ilości danych potrzebnych do ich wizualizacji, czy
eksploracji.

![Uproszczony diagram systemu]({{site.url}}/files/diagram-2017.png)

**Lista proponowanych tematów:**

<h3> A. Projekt i implementacja interfejsu programistycznego systemu
     interaktywnej wizualizacji i eksploracji danych</h3>

Celem pracy jest zaprojektowanie i implementacja interfejsu programistycznego
(API) w wybranej technologii dla systemu interaktywnej wizualizacji i
eksploracji danych. API będzie stanowiło interfejs pomiędzy relacyjną
bazą danych, a pozostałymi modułami systemy (tj. modułem
wizualizacyjnym i modułem analitycznym). Głównymi zadaniami API będzie
udostępnianie użytkownikowi możliwości wykonywania następujących operacji:

* Tworzenie i modyfikowanie struktury pi-cube na podstawie wskazanego
  źródła danych (tabela w relacyjnej bazie danych).
* Pobieranie wskazanego sparametryzowanego (za pomocą odpowiedniego
  filtra) fragmentu danych.
* Optymalizacja sposobu przesyłania danych pomiędzy komponentami, w
  taki sposób, aby zachować interaktywność systemu.

*Dodatkowe założenia i wymagania*:

* Przygotowanie zestawu testów jednostkowych do stworzonego oproramowania.
* Przetestowanie możliwości API przy użyciu istniejącej biblioteki
  wizualizacji danych (np. D3.js lub ggplot).
* Wykonanie eksperymentów przy użyciu różnych zbiorów danych (np. Checkins,
  New York Taxi Cab, Seattle Fire Calls, itp.).
* Przedstawienie wyników eksperymentów w czytelnej i zrozumiałej formie.

*Sugerowane technologie realizacji*:

* Python
* Django
* JSON

<h3> B. Implementacja interaktywnego modułu wizualizacji danych przy użyciu
     komponentu WebGL</h3>
     
Celem tego zadania jest opracowanie i implementacje interaktywnego modułu
wizualizacji danych opartego o komponent WebGL, który stanowi element
języka HTML5. Moduł powinien spełniać następujace założenia:

* Moduł powinien posiadać bibliotekę java script, za pomocą której realizowany
  będzie dostęp do modułu dostarczania danych.
* Bibliotego powinnakomunikować się z modułem dostarczania danych za pomocą
  odpowiedniego zdefiniowanego interfejsem typu RESTful.
* W celach testowych, moduł powinien umożliwiać zastąpienie odwołań do
  serwisu RESTful danymi pochodzącymi z przygotowanych wcześniej 
  plików JSON.
* Powinny być wspierane podstawowe funkcjie interfejsu wizualizacji danych,
  takie jak: *zooming in*, *zooming out*, *panning*, *selection*.

*Sugerowane technologie realizacji*:

* Java Script
* HTML5 (WebGL)
* jQuery
* Bootstrap

<h3> C. Zastosowanie indukcyjnej agregacji danych w wybranych algorytmach
     grupowania gęstościowego</h3>

Celem zadania jest zaadoptowanie (przy współpracy z opiekunem, na podstawie
dostarczonej dokumentacji oraz literatury) i zaimplementowanie koncepcji indukcyjnej
agregacji w wybranych algorytmach gęstościowego grupowania danych.

Zadaniem studenta, oprócz implementacji, będzie zaproponowanie i przeprowadzenie
odpowiednich testów, powrównujących wydajność zaprogramowanych algorytmów. 
Stworzony w ten sposób kod źródłowy  zostanie włączony jako moduł do systemu
służącego do testowania algorytmów eksploracji
danych [DMTOOLS](https://github.com/piotrlasek/clustering).

*Przykładowe zbiory testowe*:

* [Clustering datasets](https://cs.joensuu.fi/sipu/datasets/)

*Sugerowane technologie realizacji*:

* Java - implementacja algorytmów
* Python / ggplot - wizualizacja wyników

<h3> D. Projekt i implementacja progresywnego algorytmu grupowania danych</h3>

Zasada działania algorytmów progresywnych (*anytime*), polega na tym, że mogę one
zwrócić wynik nawet jeśli ich działanie zostanie przerwane. Jeśli jednak algorytm
będzie miał szansę działać dłużej, wówczas oczekiwany wynik powinien być *lepszy*.
Algorytmy tego typu okreśna się rónież niekiedy mianem algorytmów *przerywalnych*.

Zadaniem inżynieranta będzie, w opraciu o literaturę i wybrany istniejący algorytm
grupowania danych, zaprojektowanie we współpracy z opiekunem, zaimplementowanie 
oraz przetestowanie algorytmu progresywnego. Stworzony w ten sposób kod źródłowy
zostanie włączony jako moduł do systemu służącego do testowania algorytmów eksploracji
danych [DMTOOLS](https://github.com/piotrlasek/clustering).

<h3>E. Wykrywanie wzorców zachowań pacjentów na podstawie analizy wybranych zbiorów biomedycznych</h3>

Słowa kluczowe: behavioral patterns exploration, diabetes data set

<h3>F. Analiza i ocena przydatności wybranych metod wspomagania zarządzania przychodem</h3>

Słowa kluczowe: revenue management, prediction analysis

*Przykładowe zbiory testowe*:

* [Clustering datasets](https://cs.joensuu.fi/sipu/datasets/)

*Sugerowane technologie realizacji*:

* Java - implementacja algorytmów
* Python / ggplot - wizualizacja wyników

### Wybrana literatura

*Książki*

1. Tadeusz Morzy, Eksploracja Danych Metody i algorytmy, Wydawnictwo Naukowe PWN, 2017

*Artykuyły*
1. [Godfrey P., Gryz J., Lasek P.: Interactive Visualization of Large Data Sets, IEEE Transactions on Knowledge and Data Engineering (TKDE), 2016, pp 2142–2157.](http://ieeexplore.ieee.org/xpl/topAccessedArticles.jsp?punumber=69&topArticlesDate=July+2016)
2. Godfrey P., Gryz J., Lasek P., Razavi N.: Visualization through Inductive Aggregation, Proceedings of the 19th International Conference on Extending Database Technology, EDBT 2016, Bordeaux, France, March 14-18, 2016
3. Godfrey P., Gryz J., Lasek P., Razavi N.: Interactive Visualization of Big Data, Beyond Databases, Architectures, and Structures: 12th International Conference, BDAS 2016, Ustron, Poland, Springer, 2016.
4. Godfrey P., Gryz J., Lasek P., Razavi N.: Skydive: An Interactive Data Visualization Engine.  In IEEE Symposium on Large Data Analytics and Visualization, Chicago, USA, October 25-26., 2015
