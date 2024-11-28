Вежбе
======

.. questionnote::
    
    Напиши програм који проверава да ли је ученик добио петицу на тесту. Ученик је добио петицу ако је освојио више од 85 поена.

.. activecode:: grananje_vezba2
    :coach:

    poeni = int(input("Unesite broj poena: "))

    if # DOPUNI
        print("Učenik je dobio peticu.")
    else:
        print("Učenik nije dobio peticu.")



.. questionnote::
    Напиши програм који одређује да ли је број дељив са 3.

.. activecode:: grananje_vezba1
    :coach:

    broj = int(input("Unesite broj: "))

    if # DOPUNI
        print("Broj je deljiv sa 3.")
    else:
        print("Broj nije deljiv sa 3.")

.. infonote::
    **МАТЕМАТИЧКИ ПОДСЕТНИК:**


    Број је дељив са 3 ако је остатак дељења са 3 једнак 0.
    
    - 6 / 3 = 2, остатак 0
    - 7 / 3 = 2, остатак 1
    - 8 / 3 = 2, остатак 2
    - 9 / 3 = 3, остатак 0
    - 10 / 3 = 3, остатак 1
    - 11 / 3 = 3, остатак 2
    - 12 / 3 = 4, остатак 0


    6, 9 и 12 су дељиви са 3

    7, 8, 10 и 11 нису дељиви са 3


.. questionnote::
    Напиши програм који проверава да ли је број дељив са 3 и 5.

.. activecode:: grananje_vezba3
    :coach:

    broj = int(input("Unesite broj: "))

    if # DOPUNI:
        if # DOPUNI:
            print("Broj je deljiv sa 3 i 5.")
        else:
            print("Broj je deljiv sa 3, ali nije deljiv sa 5.")
    else:
        print("Broj je deljiv sa 3, ali nije deljiv sa 5.")


Дати задатак је могуће решити на више начина. Предложена структура је најдиректнија, где је идеја да се провери да ли је број дељив са 3, па ако јесте,
проверава се да ли је дељив са 5. Ако је број дељив са оба броја, онда је дељив са 3 и 5. Ако број није дељив са 5, онда није дељив и са 3 и са 5.
Исто важи и ако број није дељив са 3.

Други начин је да се користи само један `if` блок и да се проверава да ли је број дељив са 3 и 5 користећи `and` оператор. `and` оператор враћа `True` 
само ако су оба операнда `True`. То значи да број мора бити дељив са оба броја да би услов био испуњен.

.. code-block:: python

    broj = int(input("Unesite broj: "))

    if broj % 3 == 0 and broj % 5 == 0:
        print("Broj je deljiv sa 3 i 5.")
    else:
        print("Broj nije deljiv sa 3 i 5.")

Трећи начин је да се користи само један `if` блок и да се искористи својство дељивост са два броја:

Ако је број дељив са 3, онда тај број можемо изразити на следећи начин:

    :math:`broj = 3 * k`

где је `k` неки целобројни број. 

Ако је број дељив са 5, онда можемо изразити тај број на следећи начин:

    :math:`broj = 5 * l`

где је `l` неки целобројни број.

Ако је број дељив са оба броја, онда можемо изразити тај број на следећи начин:

    :math:`broj = 3 * 5 * m = 15 * m`

где је `m` неки целобројни број.

Закључак је да је број дељив са 3 и 5 ако је дељив са 15.

.. infonote::
    Број је дељив бројевима a и b ако је дељив са производом та два броја.

.. code-block:: python
    
        broj = int(input("Unesite broj: "))
    
        if broj % 15 == 0:
            print("Broj je deljiv sa 3 i 5.")
        else:
            print("Broj nije deljiv sa 3 i 5.")


.. questionnote::
    Корисник уноси температуру и временске услове (сунчано, облачно, киша). Програм треба да препоручи активност: ако је температура између 20 и 30 
    и сунчано, препоручи излет, ако је облачно или киша, препоручи читање књиге, иначе препоручи кућни одмор.

.. activecode:: grananje_vezba4
    :coach:

    temperatura = int(input("Unesi temperaturu: "))
    vreme = input("Unesi vremenske uslove (sunčano/oblačno/kiša): ").lower()

    if # DOPUNI:
        print("Preporučujemo izlet.")
    elif # DOPUNI:
        print("Preporučujemo čitanje knjige.")
    else:
        print("Preporučujemo kućni odmor.")

.. questionnote::
    Написати програм који од корисника тражи број и исписује да ли је тај број квадрат неког целог броја.

.. activecode:: grananje_vezba9
    :coach:

    broj = int(input("Unesi broj: "))

    koren = int(broj ** 0.5)

    if # DOPUNI:
        print("Broj je kvadrat nekog celog broja.")
    else:
        print("Broj nije kvadrat nekog celog broja.")

.. infonote::
    **MATЕМАТИЧКИ ПОДСЕТНИК:**

    Корен је инверзна операција степеновања. 

    Квадратни корен је инверзна операција квадратног степена (квадрата).

    .. math::

        \sqrt{9} = 3 \Rightarrow 3^2 = 9

    Да би број био квадрат неког целог броја, корен тог броја мора бити целобројни број.
    На пример, квадратни корен броја 9 је 3, што значи да је 9 квадрат броја 3, 
    док квадратни корен броја 10 није целобројни број, што значи да 10 није квадрат неког целог броја.

.. infonote::
    Резултат операције **квадратни корен** је исти као и резултат операције степеновања на 0.5.

    .. math::
            
        \sqrt{x} = x^\frac{1}{2}

    Исто правило важи за друге степене корена.

    .. math::

        \begin{align}\\
        \sqrt[3]{x} &= x^\frac{1}{3}\\
        \sqrt[4]{x} &= x^\frac{1}{4}\\
        &...
        \end{align}

.. questionnote::
    Корисник уноси цену производње мобилног телефона, као и његов оперативни систем. Направити програм који исписује продајну цену тог телефона.
    Ако је оперативни систем Андроид, на цену производње додаје се 30%, а ако је оперативни систем iOS, на цену производње додаје се 220%.

.. activecode:: grananje_vezba5
    :coach:

    cena_proizvodnje = float(input("Unesi cenu proizvodnje telefona: "))
    os = input("Unesi operativni sistem telefona (Android/iOS): ").lower()

    if # DOPUNI:
        cena = cena_proizvodnje * 1.3
    elif # DOPUNI:
        cena = cena_proizvodnje * 3.2
    else:
        cena = cena_proizvodnje

    print("Prodajna cena telefona je:", cena)

.. infonote::
    **МАТЕМАТИЧКИ ПОДСЕТНИК:**

    Ако број повећамо за 20%, то је исто као да смо додали 0.2*број на постојећи број. 

    |

    :math:`cena = cena + 0.3 * cena = cena * 1.3`

    |

    исто важи и за смањивање цене

    |

    :math:`cena = cena - 0.3 * cena = cena * 0.7` 


.. questionnote::
    Корисник уноси редни број дана у недељи (1-7). Програм треба да одреди да ли је тај дан радни или викенд. Дани 6 и 7 су викенд.


.. activecode:: grananje_vezba6
    :coach:

    dan = int(input("Unesi redni broj dana u nedelji: "))
    
    # DOPUNI

.. questionnote::
    Креирај програм за издавање паркинг карата. Цена карте зависи од типа возила и времена паркирања. 
    Аутомобил кошта 100 динара по сату, а мотор кошта 50 динара по сату. Ако се паркира дуже од 5 сати, добија се 10% попуста.

.. activecode:: grananje_vezba7
    :coach:

    tip_vozila = input("Unesi tip vozila (automobil/motor): ").lower()
    sati = int(input("Unesi broj sati parkiranja: "))

    if # DOPUNI:
        cena = 100 * sati
    else:
        cena = 50 * sati

    if #DOPUNI:
        cena = #DOPUNI
    

.. infonote::
    Функција `lower()` се користи за претварање стринга у мала слова. То значи да ако корисник унесе "Automobil" или "AUTOMOBIL" или "AuTomObiL", 
    све ће бити претворено у "automobil" и та вредност ће бити додељена променљивој `tip_vozila`.

.. questionnote::
    Креирај програм за хотел који одређује цену собе на основу типа собе и сезонских попуста. 
    
    Типови соба:
    - Стандард: 3000 динара
    - Deluxe: 5000 динара
    - Suite: 8000 динара
    
    Сезонски попусти:
    - Летњи: 0%
    - Зимски: 10%
    - Пролећни: 15%
    - Јесењи: 20%


.. activecode:: grananje_vezba8
    :coach:

    tip_sobe = input("Unesi tip sobe (standard/deluxe/suite): ").lower()
    sezona = input("Unesi sezonu (letnji/zimski/prolećni/jesenji): ").lower()

    # DOPUNI


