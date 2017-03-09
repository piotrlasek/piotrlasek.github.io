---
layout: page
title: Tematy prac inżynierskich
permalink: /for-students/tematy
exclude: true
---

# Interaktywna wizualizacja i eksploracja danych
*Tematy prac inżynierskich na semestr letni 2017*

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
**dokładny** wynik analizy (co w wielu przypadkach jest prawdą), wydaje
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
umożliwiającej dostęp do danych o zadanym stopniu granularności co
pozwala na redukcję ilości danych potrzebnych do ich wizualizacji, czy
eksploracji.

![Uproszczony diagram systemu]({{site.url}}/files/diagram-2017.png)

## Projekt i implementacja interfejsu programistycznego (API) systemu interaktywnej wizualizacji i eksploracji danych

*Cel*: Zaprojektowanie i implementacja interfejsu programistycznego
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

*Dodatkowe prace*:
* Wykonanie eksperymentów przy użyciu różnych zbiorów danych.
* xxx

*Sugerowana technologia*: Python, Django

Literatura:

1. [Godfrey P., Gryz J., Lasek P.: Interactive Visualization of Large Data Sets, IEEE Transactions on Knowledge and Data Engineering (TKDE), 2016, pp 2142–2157.](http://ieeexplore.ieee.org/xpl/topAccessedArticles.jsp?punumber=69&topArticlesDate=July+2016)
2. Godfrey P., Gryz J., Lasek P., Razavi N.: Visualization through Inductive Aggregation, Proceedings of the 19th International Conference on Extending Database Technology, EDBT 2016, Bordeaux, France, March 14-18, 2016
3. Godfrey P., Gryz J., Lasek P., Razavi N.: Interactive Visualization of Big Data, Beyond Databases, Architectures, and Structures: 12th International Conference, BDAS 2016, Ustron, Poland, Springer, 2016.
4. Godfrey P., Gryz J., Lasek P., Razavi N.: Skydive: An Interactive Data Visualization Engine.  In IEEE Symposium on Large Data Analytics and Visualization, Chicago, USA, October 25-26., 2015
