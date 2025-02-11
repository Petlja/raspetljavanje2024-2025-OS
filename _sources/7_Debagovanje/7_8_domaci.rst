Домаћи задаци
================


Примери задатака за исправку се налазе испод. Менторима је потребно да предате исправљене кодове. 


Задатак 1: Да ли је број већи од 10?
`````````````````````````````````````

.. activecode:: argumenti2200
   :coach:
   
   x = int(input("Унесите број: "))
   if x > 10
       print("x је већи од 10")


Задатак 2: Исписивање трећег елемента из листе
```````````````````````````````````````````````

.. activecode:: argumenti2201
   :coach:
   
   lista = [1, 2, 3]
   print(lista[3])


Задатак 3: Повећање броја за 10
`````````````````````````````````````

.. activecode:: argumenti2202
   :coach:
   
   broj = input("Унесите број: ")
   print(broj + 10)


Задатак 4: Исписивање свих бројева од 0 до задатог броја
````````````````````````````````````````````````````````````

.. activecode:: argumenti2205
   :coach:

   n = int(input("Унесите број: "))
   i = 0
   while i < n:
       print(i)
       i += 1
       break


Задатак 5: Исписивање чланова листе
`````````````````````````````````````

.. activecode:: argumenti2207
   :coach:

   niz = [1, 2, 3]
   for i in range(4):
       print(niz[i])


Задатак 6: Провера различитости бројева
```````````````````````````````````````

.. activecode:: argumenti2209
   :coach:

   x = int(input("Унесите први број: "))
   y = int(input("Унесите други број: "))
   if x == y:
       print("x и y су различити")


Задатак 7: Да ли је број већи од 10
```````````````````````````````````

.. activecode:: argumenti2210
   :coach:

   x = input("Унесите број: ")
   if x > 10:
       print("x је већи од 10")


Напредни задаци:
::::::::::::::::

Задатак 8: Израчунавање просека
`````````````````````````````````

.. activecode:: argumenti3001
   :coach:

   brojevi = input("Унесите бројеве одвојене размаком: ").split()
   zbir = 0
   broj_elemenata = 0

   for broj in brojevi:
       zbir += broj

   prosek = zbir / broj_elemenата
   print("Просек је:", prosek)


Задатак 9: Одређивање највећег и најмањег броја
```````````````````````````````````````````````

.. activecode:: argumenti3004
   :coach:

   brojevi = input("Унесите бројеве одвојене размаком: ").split()
   najmanji = None
   najveci = None

   for broj in brojevi:
       if broj < najmanji:
           najmanji = broj
       elif broj > najveci:
           najveci = broj

   print("Најмањи број је:", najmanji)
   print("Највећи број је:", najveci)


Задатак 10: Израчунавање збир цифара броја
```````````````````````````````````````````````

.. activecode:: argumenti3006
   :coach:

   broj = int(input("Унесите број: "))
   zbir_cifara = 0

   while broj != 0:
       zbir_cifara + broj % 10
       broj //= 10

   print("Збир цифара је:", zbir_cifara)

