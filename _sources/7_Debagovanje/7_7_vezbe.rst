Vežbe
======

Evo nekoliko primera koda sa greškama koje možete koristiti za vežbu debagovanja. Svaки пример sadrži grešku, a zatim možete pratiti korake da pronađete i ispravite grešku.

Syntaksna greška
----------------

.. activecode:: argumenti2100
   :coach:

   # Greška: zaboravljen znak za zatvaranje zagrade
   x = 5
   if x > 3:
       print("X je veći od 3"


**Koraci za debagovanje:**

1. Pokreni kod i proveri da li se pojavljuje greška.
2. Pogledaj sintaksu, zadrži pažnju na `if` uslovu.
3. Pronađi da zagrada nije zatvorena u liniji sa `print()`.
4. Dodaj zatvorenu zagradu:  `if x > 3: print("X je veći od 3")`.

Indeksna greška
----------------

.. activecode:: argumenti2101
   :coach:

   # Greška: pristup nepostojećem indeksu liste
   my_list = [1, 2, 3]
   print(my_list[5])


**Koraci za debagovanje:**

1. Pokreni kod i proveri poruku o grešci.
2. Pogledaj koja linija daje grešku: `my_list[5]`.
3. Razmisli da li lista ima toliko elemenata (u ovom slučaju, samo 3).
4. Ispravi indeks tako da bude manji od 3, npr.  `print(my_list[2])`.

Deljenje nulom
--------------

.. activecode:: argumenti2102
   :coach:

   # Greška: deljenje sa nulom
   a = 10
   b = 0
   print(a / b)


**Koraci za debagovanje:**

1. Pokreni kod i proveri poruku o grešci: `ZeroDivisionError`.
2. Pogledaj liniju sa deljenjem (`a / b`).
3. Razmisli o tome da li je  `b` 0.
4. Dodaj proveru pre deljenja:

.. activecode:: argumenti2103
   :coach:

   a = 10
   b = 0
   if b != 0:
       print(a / b)
   else:
       print("Ne može se deliti sa nulom")


Neispravno definisana promenljiva
---------------------------------

.. activecode:: argumenti2104
   :coach:

   # Greška: promenljiva nije definisana
   print(result)
   result = 5 + 3


**Koraci za debagovanje:**

1. Pokreni kod i proveri poruku o grešci: `NameError: name 'result' is not defined`.
2. Pogledaj gde koristiš promenljivu `result` pre nego što je dodeliš vrednost.
3. Premesti liniju `print(result)` nakon dodele vrednosti: 

.. activecode:: argumenti2105
   :coach:

   result = 5 + 3
   print(result)


Pogrešno poređenje
------------------

.. activecode:: argumenti2106
   :coach:
   
   # Greška: pogrešno poređenje
   x = 10
   y = 5
   if x = y:
       print("x je jednak y")


**Koraci za debagovanje:**

1. Pokreni kod i proveri poruku o grešci: `SyntaxError: invalid syntax`.
2. Pogledaj znak za poređenje. Trebalo bi da bude `==`, a ne `=`.
3. Ispravi grešku tako da bude:  `if x == y:`.

Beskonačna petlja
-----------------

.. activecode:: argumenti2107
   :coach:

   # Greška: beskonačna petlja
   i = 0
   while i < 10:
       print(i)


**Koraci za debagovanje:**

1. Pokreni kod i proveri da li se petlja beskonačno izvršava.
2. Pogledaj vrednost promenljive `i`. Nedostaje inkrementacija.
3. Dodaj inkrementaciju na kraju petlje:

.. activecode:: argumenti2108
   :coach:

   i = 0
   while i < 10:
       print(i)
       i += 1


Greška u funkciji sa vraćanjem vrednosti
----------------------------------------

.. activecode:: argumenti2109
   :coach:
   
   # Greška: funkcija ne vraća ništa
   def zbir(a, b):
       a + b

   result = zbir(3, 4)
   print(result)


**Koraci za debagovanje:**

1. Pokreni kod i proveri da li `result` bude `None`.
2. Pogledaj funkciju `zbir` i primeti da ona ne koristi `return` za vraćanje vrednosti.
3. Dodaj `return` u funkciju:

.. activecode:: argumenti2110
   :coach:

   def zbir(a, b):
       return a + b

   result = zbir(3, 4)
   print(result)
