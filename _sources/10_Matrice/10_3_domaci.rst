Домаћи задаци
:::::::::::::

Задатак 1
`````````

Napiši program koji normalizuje elemente matrice tako da svi elementi budu u opsegu [0, 1], koristeći minimalnu i maksimalnu vrednost u matrici.

**Primer 1:**

**Ulaz**:

1 2 3 

4 5 6

7 8 9

**Izlaz**:

0.0 0.125 0.25

0.375 0.5 0.625

0.75 0.875 1.0

**Objašnjenje:**

Minimalna vrednost u matrici je 1, a maksimalna vrednost je 9. Normalizacija se vrši po formuli:

:math:`x_{norm} = \frac{x - x_{min}}{x_{max} - x_{min}}`


Zadatak 2
`````````

Napiši program koji računa zbir elemenata iznad i ispod glavne dijagonale u kvadratnoj matrici.

**Primer 1:**

**Ulaz**:

1 2 3

4 5 6

7 8 9

**Izlaz**:

Zbir elemenata iznad glavne dijagonale: 15

Zbir elemenata ispod glavne dijagonale: 12

**Objašnjenje:**

Zbir elemenata iznad glavne dijagonale: 2 + 3 + 6 = 11

Zbir elemenata ispod glavne dijagonale: 4 + 7 + 8 = 19

**Primer 2:**

**Ulaz**:

1 2 3 4

5 6 7 8

9 10 11 12

13 14 15 16

**Izlaz**:

Zbir elemenata iznad glavne dijagonale: 26

Zbir elemenata ispod glavne dijagonale: 42

**Objašnjenje:**

Zbir elemenata iznad glavne dijagonale: 2 + 3 + 4 + 7 + 8 + 12 = 26

Zbir elemenata ispod glavne dijagonale: 5 + 9 + 10 + 13 + 14 + 15 = 42


Zadatak 3
`````````

Matrica predstavlja crno-belu sliku (1 - crna tačka, 0 - bela tačka). Naći dužinu najduže horizontalne, vertikalne i dijagonalne crne linije.

**Primer 1:**

**Ulaz**:

1 0 1 0 0

1 0 1 1 1

1 1 1 1 1

1 0 0 1 0

**Izlaz**:

Najduža horizontalna crna linija: 5
Najduža vertikalna crna linija: 4
Najduža dijagonalna crna linija: 3

**Primer 2:**

**Ulaz**:

1 0 1 0 0

1 0 1 1 1

1 1 1 1 1

1 0 1 1 1

1 1 1 1 1

**Izlaz**:

Najduža horizontalna crna linija: 5
Najduža vertikalna crna linija: 5
Najduža dijagonalna crna linija: 4


Задатак 4
`````````

Matrica m x n predstavlja stanovništvo u gradskim kvartovima (1 - zdravi, 2 - zaraženi, 0 - prazno). Implementiraj:

1. Simulaciju širenja zaraze gde svaki zaraženi stanovnik zarazi svoje susede (gore, dole, levo, desno).
2. Prikaz matrice posle jedne iteracije širenja.
3. Prikaz matrice posle k iteracija širenja.

**Primer 1:**

**Ulaz**:

1 1 1 1 1

1 1 1 1 1

1 1 2 1 1

1 1 1 1 1

k = 1


**Izlaz**:

1 1 1 1 1

1 1 2 1 1

1 2 2 2 1

1 1 2 1 1

**Objašnjenje:**

Zaraženi stanovnik u sredini zarazio je svoje susede. 

**Primer 2:**

**Ulaz**:

1 1 1 1 1

1 1 1 1 1

1 1 2 1 1

1 1 2 1 1

k = 2

**Izlaz**:

1 1 2 1 1

1 2 2 2 1

2 2 2 2 2

2 2 2 2 2

**Objašnjenje:**

Zaraženi stanovnik u sredini zarazio je svoje susede koji su u dugoj iteraciji zarazili svoje susede.


Задатак 5
`````````

Matrica sadrži samo 0 i 1. Pronađi najveći pravougaonik koji se sastoji isključivo od 1 и израчунај његову површину.

**Primer 1:**

**Ulaz**:

1 0 1 0 0

1 0 1 1 1

1 1 1 1 1

1 0 0 1 0

**Izlaz**:

6

**Objašnjenje:**

Najveći pravougaonik koji se sastoji isključivo od 1 je:

1 0 1 0 0

1 0 **1 1 1**

1 1 **1 1 1**

1 0 0 1 0

**Primer 2:**

**Ulaz**:

1 0 1 0 0

1 0 1 1 1

1 1 1 1 1

1 0 1 1 1

1 1 1 1 1

**Izlaz**:

12

**Objašnjenje:**

Najveći pravougaonik koji se sastoji isključivo od 1 je:

1 0 1 0 0

1 0 **1 1 1**

1 1 **1 1 1**

1 0 **1 1 1**

1 1 **1 1 1**


Задатак 6
`````````

Pao je sneg u gradu i potrebno je znati koliko centimetra snega je u kom delu grada palo. 
Na nekim delovima grada je izmereno koliko je palo snega, dok na drugim delovima nije. 
Imamo delimično popunjenu matricu gde svaki element predstavlja lokaciju u gradu i koliko centimetara snega je palo na toj lokaciji. 
Lokacije na kojima je izmerena visina snega imaju broj između 1 i 10 dok lokacije na kojima nije izmereno imaju vrednost 0. 
Potrebno je napraviti program koji za unete koordinate matrice estimira koliko je snega palo na toj lokaciji. 
Visina snega u nekom polju se estimira kao prosečna vrednost lokacija oko nje koje imaju izmerenu visinu snega (srednja vrednost 3x3 podmatrice čiji je centar u traženoj tački). 
Ako tražena tačka niji i jedno polje oko nje nemaju izmerenu visinu snega matrica pretrage se proširuke na dimenzije 5x5. 
Ako ni tad nema proširuje se na 7x7 itd...

**Primer 1:**

**Ulaz**:

0 2 1 0 0 5 0 0 0

0 1 0 5 0 0 0 0 0

0 0 0 0 4 0 3 0 0

0 3 5 0 0 5 1 0 0

0 0 4 0 0 0 0 0 0

0 0 0 0 0 0 0 0 0

Koordinate: (2, 1)

**Izlaz**:

Estimirana visina snega: 22.5

**Objašnjenje:**

0 2 1 0 0 5 0 0 0

0 1 **0** 5 0 0 0 0 0

0 0 0 0 4 0 3 0 0

0 3 5 0 0 5 1 0 0

0 0 4 0 0 0 0 0 0

0 0 0 0 0 0 0 0 0

Estimirana visina: (2 + 1  + 1 + 5) / 4 = 2.25

**Primer 2:**

ista matrica kao u primeru 1

Koordinate: (5, 4)

**Izlaz**:

Estimirana visina snega: 3.0

**Objašnjenje:**

0 2 1 0 0 5 0 0 0

0 1 0 5 0 0 0 0 0

0 0 0 0 4 0 3 0 0

0 3 5 0 0 5 1 0 0

0 0 4 0 0 0 0 0 0

0 0 0 0 0 **0** 0 0 0

Okolina 3x3 je prazna pa se okolina proširuje na 5x5. Prosečna vrednost izmerenih tačaka u okolini 5x5 je (5 + 1) / 2 = 3.0


Zadatak 7
`````````

**UPOZORENJE:** Ovaj zadatak je napredan zadatak.

|

Matrica dimenzija m x n predstavlja raspored parking mesta (1 - zauzeto, 0 - slobodno). 
Za date koordinate odrediti da li je parking mesto slobodno. 
Parking mesto je slobodno ako nije zauzeto i do njega može da se dođe (ima put nula od te tačke do ivice matrice).

**Primer 1:**

**Ulaz**:

1 1 1 1 1

1 0 0 0 0

1 1 1 1 1

1 0 0 0 1

1 1 1 1 1

Koordinate: (2, 2)

**Izlaz**:

Parking mesto je slobodno

**Objašnjenje:**

1 1 1 1 1

1 **0** 0 0 0

1 1 1 1 1

1 0 0 0 1

1 1 1 1 1

Parking mesto je slobodno jer se može doći do ivice matrice.

**Primer 2:**

**Ulaz**:

1 1 1 1 1

1 0 0 0 0

1 1 1 1 1

1 0 0 0 1

1 1 1 1 1

Koordinate: (4, 3)

**Izlaz**:

Parking mesto nije slobodno

**Objašnjenje:**

1 1 1 1 1

1 0 0 0 0

1 1 1 1 1

1 0 0 **0** 1

1 1 1 1 1

Parking mesto nije slobodno jer se ne može doći do ivice matrice preko slobodnih pozicija.




