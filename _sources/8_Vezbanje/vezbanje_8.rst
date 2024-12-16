Вежбање
==============

.. questionnote ::

   Написати функцију min(x, y, z) која израчунава минимум три броја. Функцију написати
   на два начина, једном коришћењем листи, други пут без коришћења листи.
   Написати програм који учитава три цела броја и исписује њихов минимум.

Ево како се може написати функција `min` на два начина:  

1. **Коришћењем листе**  
2. **Без коришћења листе** 

Решење са листом:

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

Објашњење:

- У првом решењу, користимо Пајтонову функцију `min` на листи која садржи бројеве 

- У другом решењу, ручно проналазимо најмању вредност помоћу if-услова 

Оба програма омогућавају унос три броја и исписују најмањи број коришћењем одговарајуће функције.

-------------------------------------------------------------------

.. questionnote ::

   Написати функцију која рачуна квадрат унетог броја
   
   
Једноставна функција која рачуна квадрат унетог броја:

.. activecode:: vezbanje8_102
   :coach:
   
   def kvadrat(broj):
       return broj ** 2

   # Program koji koristi funkciju
   broj = float(input("Unesite broj: "))
   print("Kvadrat broja", broj, "je:", kvadrat(broj))


Објашњење:
1. Функција `kvadrat` прима један аргумент `broj`.
2. Користи оператор `**` за израчунавање квадрата броја.
3. Корисник уноси број који се затим прослеђује функцији, а резултат се исписује.
 

Можете користити ову функцију за израчунавање квадрата било ког броја, укључујући целе бројеве и децималне вредности.   
   
 
.. questionnote :: 
   
   Написати функцију која рачуна апсолутну вредност унетог броја
   
   
Функција за рачунање апсолутне вредности

.. activecode:: vezbanje8_103
   :coach:

   def apsolutna_vrednost(broj):
       if broj < 0:
           return -broj
       return broj

   # Program koji koristi funkciju
   broj = float(input("Unesite broj: "))
   print("Apsolutna vrednost broja", broj, "je:", apsolutna_vrednost(broj))

Објашњење:
1. Функција `apsolutna_vrednost` прима један аргумент `broj`.
2. Ако је број негативан (`broj < 0`), враћа супротну вредност броја (`-broj`).
3. Ако је број позитиван или нула, враћа се број без измене.
4. Програм омогућава унос броја од стране корисника и исписује његову апсолутну вредност.   
   

.. questionnote ::

   Написати функцију која рачуна куб унетог броја
   

Функција за рачунање куба

.. activecode:: vezbanje8_104
   :coach:

   def kub(broj):
       return broj ** 3

   # Program koji koristi funkciju
   broj = float(input("Unesite broj: "))
   print("Kub broja", broj, "je:", kub(broj))

Објашњење:

1. Функција `kub` прима један аргумент `broj`

2. Користи оператор `**` за израчунавање трећег степена (куба) броја

3. Корисник уноси број, који се прослеђује функцији, а резултат се исписује   
   

.. questionnote ::

   Написати функцију која рачуна x^n где су x и n аргументи функције
   

Функција за рачунање  x^ n

.. activecode:: vezbanje8_105
   :coach:

   def stepen(x, n):
       return x ** n

   # Program koji koristi funkciju
   x = float(input("Unesite osnovu x: "))
   n = int(input("Unesite eksponent n: "))
   print("Rezultat", x, "podignut na", n, "je:", stepen(x, n))

Објашњење:

1. Функција `stepen` прима два аргумента: `x` (основа) и `n` (експонент)

2. Користи оператор `**` за израчунавање x^n

3. Корисник уноси основу и експонент, који се затим прослеђују функцији, а резултат се исписује   

Функција за рачунање x^n са петљом

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

Објашњење:

1. Функција `stepen_petlja` користи петљу за множење основе `x` са самом собом `n` пута

2. Ако је експонент негативан (`n < 0`), функција изврши инверзију резултата x^(-n) = 1/x^n

3. Петља користи `abs(n)` да би избегла грешку са негативним бројевима, а затим резултат коригује ако је експонент негативан

Овај начин рачунања x^n користи петљу уместо оператора '**', што може бити корисно за веће вредности експонента

.. questionnote ::

   Написати функцију која рачуна Фибоначијев низ
   

Фибоначијев низ (итеративни приступ)

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


Објашњење:

1. Ако је n <= 1, функција одмах враћа n (јер су први и други број у Фибоначијевом низу 0 и 1)

2. За вредности н > 1, користи се петља која рачуна n-ти Фибоначијев број. Почетне вредности су `а = 0` и `b = 1`

3. У свакој итерацији, `а` постаје претходни број низа, а `b` постаје тренутни број низа, док се број који треба да се израчуна помера за једно место у низу

4. На крају, функција враћа последњи број који је израчунат у петљи

Објашњење:

Овај приступ користи променљиве `а` и `b` за чување претходна два броја низа и итерира кроз петљу да израчуна n-ти број Фибоначијевог низа
   
   
.. questionnote ::

   Написати програм који тестира ове функције
   
   
Ево програма који тестира све функције које смо претходно написали: 

1. Функција која рачуна квадрат броја.
2. Функција која рачуна апсолутну вредност броја.
3. Функција која рачуна куб броја.
4. Функција која рачуна x^n(степен).
5. Функција која рачуна Фибоначијев низ.


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

Објашњење:

1. Програм тестира сваку од функција: квадрат, апсолутну вредност, куб, степен и Фибоначијев низ

2. За сваку функцију корисник уноси одговарајући број или вредности, а затим програм исписује резултат

3. Све функције су позване у оквиру тестирања, како би се проверило њихово исправно функционисање са корисничким уносом   

