Вежбе
======

Ево неколико примера кода са грешкама које можете користити за вежбу дебаговања. Сваки пример садржи грешку, а затим можете пратити кораке да пронађете и исправите грешку.

Синтаксна грешка
----------------

.. activecode:: argumenti2100
   :coach:

   # Greška: zaboravljen znak za zatvaranje zagrade
   x = 5
   if x > 3:
       print("X je veći od 3"


**Кораци за дебаговање:**

1. Покрени кôд и провери да ли се појављује грешка.
2. Погледај синтаксу, задржи пажњу на `if` услову.
3. Пронађи да заграда није затворена у линији са `print()`.
4. Додај затворену заграду:  `if x > 3: print("X je veći od 3")`.

Индексна грешка
----------------

.. activecode:: argumenti2101
   :coach:

   # Greška: pristup nepostojećem indeksu liste
   my_list = [1, 2, 3]
   print(my_list[5])


**Кораци за дебаговање:**

1. Покрени кôд и провери поруку о грешци.
2. Погледај која линија даје грешку: `my_list[5]`.
3. Размисли да ли листа има толико елемената (у овом случају, само 3).
4. Исправи индекс тако да буде мањи од 3, нпр.  `print(my_list[2])`.

Дељење нулом
--------------

.. activecode:: argumenti2102
   :coach:

   # Greška: deljenje sa nulom
   a = 10
   b = 0
   print(a / b)


**Кораци за дебаговање:**

1. Покрени кôд и провери поруку о грешци: `ZeroDivisionError`.
2. Погледај линију са дељењем (`a / b`).
3. Размисли о томе да ли је  `b` = 0.
4. Додај проверу пре дељења:

.. activecode:: argumenti2103
   :coach:

   a = 10
   b = 0
   if b != 0:
       print(a / b)
   else:
       print("Ne može se deliti sa nulom")


Неисправно дефинисана променљива
---------------------------------

.. activecode:: argumenti2104
   :coach:

   # Greška: promenljiva nije definisana
   print(result)
   result = 5 + 3


**Кораци за дебаговање:**

1. Покрени кôд и провери поруку о грешци: `NameError: name 'result' is not defined`.
2. Погледај где користиш променљиву `result` пре него што је доделиш вредност.
3. Премести линију `print(result)` након доделе вредности: 

.. activecode:: argumenti2105
   :coach:

   result = 5 + 3
   print(result)


Погрешно поређење
------------------

.. activecode:: argumenti2106
   :coach:
   
   # Greška: pogrešno poređenje
   x = 10
   y = 5
   if x = y:
       print("x je jednak y")


**Кораци за дебаговање:**

1. Покрени кôд и провери поруку о грешци: `SyntaxError: invalid syntax`.
2. Погледај знак за поређење. Требало би да буде `==`, а не `=`.
3. Исправи грешку тако да буде:  `if x == y:`.

Бесконачна петља
-----------------

.. activecode:: argumenti2107
   :coach:

   # Greška: beskonačna petlja
   i = 0
   while i < 10:
       print(i)


**Кораци за дебаговање:**

1. Покрени кôд и провери да ли се петља бесконачно извршава.
2. Погледај вредност променљиве `i`. Недостаје инкрементација.
3. Додај инкрементацију на крају петље:

.. activecode:: argumenti2108
   :coach:

   i = 0
   while i < 10:
       print(i)
       i += 1


Грешка у функцији са враћањем вредности
----------------------------------------

.. activecode:: argumenti2109
   :coach:
   
   # Greška: funkcija ne vraća ništa
   def zbir(a, b):
       a + b

   result = zbir(3, 4)
   print(result)


**Кораци за дебаговање:**

1. Покрени кôд и провери да ли `result` буде `None`.
2. Погледај функцију `zbir` и примети да она не користи `return` за враћање вредности.
3. Додај `return` у функцију:

.. activecode:: argumenti2110
   :coach:

   def zbir(a, b):
       return a + b

   result = zbir(3, 4)
   print(result)
