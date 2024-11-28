Вежбе
======

У наставку су наведени задаци који се фокусирају на коришћење функција `input()` и `print()`, као и рад са различитим типовима података у Python-у.


.. questionnote:: **Задатак 1:**
	

	Напиши програм који од корисника захтева да унесе своје име, а затим ће га исписати.

	Пример улаза:
	`Марко`

	Пример излаза:
	`Ваше име је: Марко`

.. activecode:: osnove_vezbe1
	:coach:

	ime = input("Unesite svoje ime: ")
	# DOPUNI

.. questionnote:: **Задатак 2:**
	

	Напиши програм који од корисника захтева да унесе своје име и презиме. Програм треба да их споји и прикаже у формату: `Име Презиме`.

	Пример улаза:  
	Марија  
	Тодоровић

	Пример излаза:  
	Пуно име: Марија Тодоровић

.. activecode:: osnove_vezbe2
	:coach:

	ime = input("Unesite svoje ime: ")
	prezime = input("Unesite svoje prezime: ")
	# DOPUNI





.. mchoice:: uvod_vezbe_pitanje_1
	:answer_a: 52
	:answer_b: 3517
	:answer_c: 35 17
	:answer_d: 52 17
	:correct: b

	Шта ће бити исписано на излазу наведеног програма ако је на улазу унето 35 и 17?

	.. code-block:: python

		a = input()
		b = input()
		print(a+b)



.. mchoice:: uvod_vezbe_pitanje_2
	:answer_a: 52
	:answer_b: 3517
	:answer_c: 35 17
	:answer_d: 52 17
	:correct: a

	Шта ће бити исписано на излазу наведеног програма ако је на улазу унето 35 и 17?
	
	.. code-block:: python

		a = int(input())
		b = int(input())
		print(a+b)



.. questionnote:: **Задатак 3:**
	

	Напиши програм који од корисника захтева да унесе своје године. Програм треба да конвертује године у месеце (1 година = 12 месеци) и прикаже резултат.

	Пример улаза:  
	25

	Пример излаза:  
	`Ваших 25 година је једнако 300 месеци.`

.. activecode:: osnove_vezbe3
	:coach:

	godine = int(input("Unesite svoje godine: "))
	meseci = # DOPUNI
	print("Vasih", godine, "godina je jednako", meseci, "meseci.")



.. questionnote:: **Задатак 4:**

	Напиши програм који од корисника захтева да унесе два цела броја. Програм треба да израчуна и прикаже њихов збир.

	Пример улаза:  
	8  
	12

	Пример излаза:  
	Збир бројева 8 и 12 је 20.

.. activecode:: osnove_vezbe4
	:coach:

	broj1 = # DOPUNI
	broj2 = # DOPUNI
	zbir = # DOPUNI
	print("Zbir brojeva", broj1, "i", broj2, "je", zbir, ".")


.. questionnote:: **Задатак 5:**

	
	Напиши програм који од корисника захтева да унесе температуру у Целзијусима и конвертује је у Фаренхајте. Прикажи резултат у формату: `Температура у Фаренхајтима је: ...`.
	
	|

	:math:`F = \frac{9}{5} \cdot C + 32`

	|

	Пример улаза:  
	25

	Пример излаза:  
	Температура у Фаренхајтима је: 77.0.

.. activecode:: osnove_vezbe5
	:coach:

	celsius = float(input("Unesite temperaturu u Celzijusima: "))
	fahrenheit = # DOPUNI
	print("Temperatura u Farenhajtima je:", fahrenheit, ".")



.. mchoice:: uvod_vezbe_pitanje_3
	:answer_a: 12
	:answer_b: 170
	:answer_c: 35
	:answer_d: 23
	:correct: d

	Шта ће бити исписано на излазу наведеног програма?

	.. code-block:: python

		x = 3
		y = 4
		z = 5
		rezultat = x + y * z
		print(rezultat)

.. questionnote:: **Задатак 6:**
	
	Исправи наведени кôд (без мењања бројева) тако да на излазу буде исписано 35.

.. activecode:: osnove_vezbe6
	:coach:
	
	x = 3
	y = 4
	z = 5
	rezultat = x + y * z
	print(rezultat)

Правила предности алгебарских операција у Python-у су иста као у математици.

.. questionnote:: **Задатак 7:**
	

	Напиши програм који од корисника захтева да унесе полупречник круга. Израчунај и прикажи површину круга. Формула за површину је:  
	
	|

	:math:`P = \pi \cdot r^2`

	(можеш користити `3.14` за π)

	|

	Пример улаза:  
	5

	Пример излаза:  
	Површина круга са радијусом 5 је: 78.5.

.. activecode:: osnove_vezbe7
	:coach:

	radius = float(input("Unesite poluprecnik kruga: "))
	area = # DOPUNI
	print("Povrsina kruga sa radijusom", radius, "je:", area, ".")


.. questionnote:: **Задатак 8:**

	Напиши програм који од корисника захтева да унесе три оцене. Програм треба да израчуна и прикаже просечну оцену.

	Пример улаза:  
	3  
	4  
	5

	Пример излаза:  
	Ваша просечна оцена је: 4.0


.. activecode:: osnove_vezbe8
	:coach:

	ocena1 = # DOPUNI
	ocena2 = # DOPUNI
	ocena3 = # DOPUNI
	prosek = # DOPUNI
	print("Tvoj prosek je: " + str(prosek))

Унутар исписа датог програма смо спојили текст и број у један стринг тако што смо број претворили у стринг и повезали их операцијом сабирања. 
Исти испис би био постигнут да смо само написали `print("Tvoj prosek je: ", prosek)`.

.. questionnote:: **Задатак 9:**

	Напиши програм који исписује само последњу цифру датог броја.

	Пример улаза:
	`123`

	Пример излаза:
	`Poslednja cifra broja 123 je 3`

.. activecode:: osnove_vezbe9
	:coach:

	broj = int(input("Unesite broj: "))
	poslednja_cifra = # DOPUNI
	print("Poslednja cifra broja", broj, "je", poslednja_cifra)

Када се тражи израчунавање последње цифре броја, можемо користити операцију остатка при дељењу са 10. 
Остатак при дељењу са 10 је управо последња цифра броја.

:math:`123 = 12 \cdot 10 + 3`

:math:`123 \% 10 = 3`

|

На сличан начин се могу индивидуално издвајати и друге цифре броја. На пример:

Другу цифру броја можемо добити као остатак при дељењу са 100 и целобројним дељењем са 10.

.. math::

	\begin{align}\\
	&123 = 1 \cdot 100 + 2 \cdot 10 + 3 = 1 \cdot 100 + 23\\
	&123 \% 100 = 23\\
	&23 // 10 = 2\\
	\end{align}

Остале цифре се добијају на сличан начин следећом формулом:

.. math::
	
	a_i = (n \% 10^i) // 10^{i-1}

|

где је :math:`a_i` :math:`i`-та цифра броја, а :math:`n` број.

.. infonote::
	У Python-у, операција **степен** означава се са `**`. На пример, `10**2` представља 10 на квадрат.

.. infonote:: **МАТЕМАТИЧКИ ПОДСЕТНИК:**

	Операција степеновања означава множење броја самог са собом одређени број пута. 
	На пример, :math:`10^2` представља 10 на квадрат, што значи 10 пута 10, односно 100.
	
	.. math::
		
		\begin{align}\\
		&10^2 = 10 \cdot 10 = 100\\
		&10^3 = 10 \cdot 10 \cdot 10 = 1000\\
		&5^3 = 5 \cdot 5 \cdot 5 = 125\\
		&2^4 = 2 \cdot 2 \cdot 2 \cdot 2 = 16\\
		\end{align}









