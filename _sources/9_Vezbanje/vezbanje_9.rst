Вежбање
==============

.. questionnote ::

   Napisati funkciju min(x, y, z) koja izračunava minimum tri broja. Funkciju napisati
   na dva načina, jednom korišćenjem listi, drugi put bez korišćenja listi.
   Napisati program koji učitava tri cela broja i ispisuje njihov minimum.


Evo kako se može napisati funkcija `min` na dva načina:  

1. **Korišćenjem liste**  
2. **Bez korišćenja liste** 

Rešenje sa listom:

.. activecode:: vezbanje8_100
   :coach:

   def min_with_list(x, y, z):
       return min([x, y, z])

   # Program koji koristi funkciju sa listom
   x = int(input("Unesite prvi broj: "))
   y = int(input("Unesite drugi broj: "))
   z = int(input("Unesite treći broj: "))

   print("Minimum tri broja je (koristeći listu):", min_with_list(x, y, z))


Rešenje bez liste:

.. activecode:: vezbanje8_101
   :coach:
   
   def min_without_list(x, y, z):
       min_value = x
       if y < min_value:
           min_value = y
       if z < min_value:
           min_value = z
       return min_value

   # Program koji koristi funkciju bez liste
   x = int(input("Unesite prvi broj: "))
   y = int(input("Unesite drugi broj: "))
   z = int(input("Unesite treći broj: "))

   print("Minimum tri broja je (bez liste):", min_without_list(x, y, z))


Objašnjenje:

U prvom rešenju, koristimo Pythonovu funkciju `min` na listi koja sadrži brojeve 

1. Funkcija `zapis(x, y)` pretvara oba broja x i y u stringove kako bi im se mogla pristupiti svaka cifra.

U drugom rešenju, ručno pronalazimo najmanju vrednost pomoću if-uslova 

Oba programa omogućavaju unos tri broja i ispisuju najmanji broj korišćenjem odgovarajuće funkcije.
3. Ako su sortirane cifre oba broja iste, funkcija vraća 1, što znači da brojevi koriste iste cifre. U suprotnom, vraća 0.

-------------------------------------------------------------------


.. questionnote ::

   Napisatu funkciju koja računa kvadrat unetog broja
   
   
Jednostavna funkcija koja računa kvadrat unetog broja:

.. activecode:: vezbanje8_102
   :coach:
   
   def kvadrat(broj):
       return broj ** 2

   # Program koji koristi funkciju
   broj = float(input("Unesite broj: "))
   print("Kvadrat broja", broj, "je:", kvadrat(broj))



Objašnjenje:
1. Funkcija `kvadrat` prima jedan argument `broj`.
2. Koristi operator `**` za izračunavanje kvadrata broja.
3. Korisnik unosi broj koji se zatim prosleđuje funkciji, a rezultat se ispisuje.
 

Možete koristiti ovu funkciju za izračunavanje kvadrata bilo kog broja, uključujući cele brojeve i decimalne vrednosti.    
   
 
.. questionnote :: 
   
   Napisati funkciju koja računa apsolutnu vrednost unetog broja
   
   
Funkcija za računanje apsolutne vrednosti

.. activecode:: vezbanje8_103
   :coach:

   def apsolutna_vrednost(broj):
       if broj < 0:
           return -broj
       return broj

   # Program koji koristi funkciju
   broj = float(input("Unesite broj: "))
   print("Apsolutna vrednost broja", broj, "je:", apsolutna_vrednost(broj))


Objašnjenje:
1. Funkcija `apsolutna_vrednost` prima jedan argument `broj`.
2. Ako je broj negativan (`broj < 0`), vraća suprotnu vrednost broja (`-broj`).
3. Ako je broj pozitivan ili nula, vraća se broj bez izmene.
4. Program omogućava unos broja od strane korisnika i ispisuje njegovu apsolutnu vrednost.   
   

.. questionnote ::

   Napisati funkciju koja računa kub unetog broja
   

Funkcija za računanje kuba

.. activecode:: vezbanje8_104
   :coach:

   def kub(broj):
       return broj ** 3

   # Program koji koristi funkciju
   broj = float(input("Unesite broj: "))
   print("Kub broja", broj, "je:", kub(broj))


Objašnjenje:

1. Funkcija `kub` prima jedan argument `broj`

2. Koristi operator `**` za izračunavanje trećeg stepena (kuba) broja
2. Zatim proverava svaku cifru u stringu. Ako se dve uzastopne cifre (u paru) ponašaju na isti način obe su parne ili obe su neparne, vraća 0, što znači da cifre nisu 
naizmenično parne i neparne

3. Ako su sve cifre naizmenično parne i neparne, funkcija vraća 1

4. Program koristi ovu funkciju da proveri uneti broj i ispiše odgovarajući rezultat

3. Korisnik unosi broj, koji se prosleđuje funkciji, a rezultat se ispisuje   
   

.. questionnote ::

   Napisati funkciju koja računa x^n gde su x i n argumenti funkcije
   

Funkcija za računanje  x^n

.. activecode:: vezbanje8_105
   :coach:

   def stepen(x, n):
       return x ** n

   # Program koji koristi funkciju
   x = float(input("Unesite osnovu x: "))
   n = int(input("Unesite eksponent n: "))
   print("Rezultat", x, "podignut na", n, "je:", stepen(x, n))


Objašnjenje:

1. Funkcija `stepen` prima dva argumenta: `x` (osnova) i `n` (eksponent)

2. Koristi operator `**` za izračunavanje x^n

3. Korisnik unosi osnovu i eksponent, koji se zatim prosleđuju funkciji, a rezultat se ispisuje   


Funkcija za računanje x^n sa petljom

.. activecode:: vezbanje8_106
   :coach:

   def stepen_petlja(x, n):
       rezultat = 1
       for i in range(abs(n)):  # Iterira n puta
           rezultat *= x  # Množi osnovu x n puta
       if n < 0:  # Ako je eksponent negativan, invertuje rezultat
           rezultat = 1 / rezultat
       return rezultat

   # Program koji koristi funkciju
   x = float(input("Unesite osnovu x: "))
   n = int(input("Unesite eksponent n: "))
   print("Rezultat", x, "podignut na", n, "je:", stepen_petlja(x, n))


Objašnjenje:

1. Funkcija `stepen_petlja` koristi petlju za množenje osnove `x` sa samom sobom `n` puta

2. Ako je eksponent negativan (`n < 0`), funkcija izvrši inverziju rezultata x^(-n) = 1/x^n

3. Petlja koristi `abs(n)` da bi izbegla grešku sa negativnim brojevima, a zatim rezultat koriguje ako je eksponent negativan


Ovaj način računanja x^n koristi petlju umesto operatora '**', što može biti korisno za veće vrednosti eksponenta


.. questionnote ::

   Napisati funkciju koja računa fibonačijev niz
   

Fibonacci niz (iterativni pristup)

.. activecode:: vezbanje8_107
   :coach:

   def fibonaci(n):
    if n <= 1:
        return n
    a, b = 0, 1
    for i in range(2, n + 1):
        a, b = b, a + b
    return b

   # Program koji koristi funkciju
   n = int(input("Unesite broj n: "))
   print("Rezultat: ", n, "-ti broj Fibonacci niza je:", fibonaci(n))



Objašnjenje:

1. Ako je n <= 1, funkcija odmah vraća n (jer su prvi i drugi broj u Fibonacci nizu 0 i 1)

2. Za vrednosti n > 1, koristi se petlja koja računa n-ti Fibonacci broj. Početne vrednosti su `a = 0` i `b = 1`

3. U svakoj iteraciji, `a` postaje prethodni broj niza, a `b` postaje trenutni broj niza, dok se broj koji treba da se izračuna pomera za jedno mesto u nizu

4. Na kraju, funkcija vraća poslednji broj koji je izračunat u petlji


Objašnjenje:

Ovaj pristup koristi promenljive `a` i `b` za čuvanje prethodna dva broja niza i iterira kroz petlju da izračuna n-ti broj Fibonacci niza
   
   
.. questionnote ::

   Napisati program koji testira ove funkcije
   
   
Evo programa koji testira sve funkcije koje smo prethodno napisali: 

1. Funkcija koja računa kvadrat broja.
2. Funkcija koja računa apsolutnu vrednost broja.
3. Funkcija koja računa kub broja.
4. Funkcija koja računa x^n(stepen).
5. Funkcija koja računa Fibonacci niz.



.. activecode:: vezbanje8_108
   :coach:


   # Funkcija za kvadrat broja
   def kvadrat(broj):
       return broj ** 2

   # Funkcija za apsolutnu vrednost broja
   def apsolutna_vrednost(broj):
       if broj < 0:
           return -broj
       return broj

   # Funkcija za kub broja
   def kub(broj):
       return broj ** 3

   # Funkcija za računanje x^n
   def stepen(x, n):
       return x ** n

   # Funkcija za Fibonacci niz
   def fibonaci(n):
       if n <= 1:
           return n
       a, b = 0, 1
       for i in range(2, n + 1):
           a, b = b, a + b
       return b

   # Testiranje svih funkcija
   print("Testiranje funkcija:")

   # Testiranje kvadrata
   broj = float(input("Unesite broj za kvadrat: "))
   print("Kvadrat broja", broj, "je:", kvadrat(broj))

   # Testiranje apsolutne vrednosti
   broj = float(input("Unesite broj za apsolutnu vrednost: "))
   print("Apsolutna vrednost broja", broj, "je:", apsolutna_vrednost(broj))

   # Testiranje kuba
   broj = float(input("Unesite broj za kub: "))
   print("Kub broja", broj, "je:", kub(broj))

   # Testiranje stepena x^n
   x = float(input("Unesite osnovu x za x^n: "))
   n = int(input("Unesite eksponent n za x^n: "))
   print(x, "podignut na", n, "je:", stepen(x, n))

   # Testiranje Fibonacci niza
   n = int(input("Unesite broj n za Fibonacci niz: "))
   print(n, "-ti broj Fibonacci niza je:", fibonaci(n))


Objašnjenje:

1. Program testira svaku od funkcija: kvadrat, apsolutnu vrednost, kub, stepen i Fibonacci niz

2. Za svaku funkciju korisnik unosi odgovarajući broj ili vrednosti, a zatim program ispisuje rezultat
1. Funkcija `romb(n)` prvo proverava da li je n pozitivan broj. Ako nije, ispisuje poruku o grešci

2. Prvi deo funkcije iscrtava gornji deo romba. To se radi tako što za svaki red broj zvezda raste od 1 ka 2n-1, a broj praznog prostora na početku svakog 
reda opada

3. Sve funkcije su pozvane u okviru testiranja, kako bi se proverilo njihovo ispravno funkcionisanje sa korisničkim unosom   