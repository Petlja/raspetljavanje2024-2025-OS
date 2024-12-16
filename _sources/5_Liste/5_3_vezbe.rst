Вежбе
======

У овој вежби фокусираћемо се на различите аспекте рада са листама у Python-у. Ове вежбе покривају основне операције са листама, укључујући креирање, додавање, уклањање и претрагу елемената.

.. Zadatak 0

.. infonote::

    До сада смо, када је потребно унети више бројева, бројеве уносили један по један. Постоји много елегантнији начин да се уносе бројеви у листу. 
    У Python-у је могуће унети више бројева одједном користећи функцију `input` и функцију `split`. 
    Функција `split` раздваја унете бројеве на основу размака и креира листу од њих.

    .. code-block:: python

        brojevi = input('Unesite brojeve razdvojene razmakom: ').split()

    У овом примеру корисник уноси бројеве раздвојене размаком, на пример `1 2 3 4`, и они се уносе у листу `brojevi`.

    |

    Такође је могуће користити друге кључне карактере за раздвајање бројева, као што су запета, тачка, зарез итд. 
    Ако није унет аргумент функције `split`, раздвајање се врши на основу размака.

    .. code-block:: python

        brojevi = input('Unesite brojeve razdvojene zarezom: ').split(',')

    У овом примеру корисник уноси бројеве раздвојене зарезом, на пример `1,2,3,4`, и они се уносе у листу `brojevi`.



.. ZADATAK 1
.. questionnote::

    Креирај листу са најмање 5 различитих животиња и испиши сваку животињу у новом реду.

.. activecode:: liste_vezba1
    :coach:

    zivotinje = ['mačka', 'pas', 'konj', 'tigar', 'slon']
    # DOPUNI

Овај задатак може се решити на више начина. Један од начина је коришћење петље `for`:
- могуће је итерирати кроз елементе листе и исписати их један по један.
- могуће је итерирати кроз индексе листе и исписати елементе листе на основу индекса.


.. ZADATAK 2
.. questionnote::

    Напиши задатак који за унети број `n` креира листу `[1, 2, 3, ..., n]` и исписује је.

.. activecode:: liste_vezba2
    :coach:

    n = int(input('Unesite broј n: '))
    brojevi = []
    
    for i in range(1, n + 1):
        # DOPUNI
    
    print(brojevi)

.. learnmorenote::

    Напредни начин решавања

    Овај задатак могуће је решити користећи функцију `range` која креира листу бројева од 1 до `n`. 
    Ако користимо овај приступ, потребно је да претворимо излаз функције `range` у листу јер оно што добијамо је објекат класе `range`:

    .. code-block:: python

        brojevi = list(range(1, n + 1))

.. ZADATAK 3
.. questionnote::

    Креирај листу са неколико имена. Уклони последњи елемент из листе, додај нов елемент на крај листе, а затим додај нови елемент на 2. место.

.. activecode:: liste_vezba3
    :coach:

    imena = ['Marko', 'Ana', 'Jovan', 'Mira', 'Petar']
    # DOPUNI
    prvo_novo_ime = input('Unesi novo ime: ')
    # DOPUNI
    drugo_novo_ime = input('Unesi drugo novo ime: ')
    # DOPUNI
    print('Nova lista:', imena)

.. infonote::

    Да би се нови елемент додао усред листе, потребно је да се сви елементи после њега "помере у десно".
    На пример, ако имамо листу [1, 2, 3, 4] и желимо да додамо број 5 на друго место, нова листа ће изгледати овако: [1, 5, 2, 3, 4].
    Приметимо да се сви елементи после 5 померају за једно место удесно (2 се помера са индекса 1 на индекс 2, 3 са индекса 2 на индекс 3, итд.).


.. ZADATAK 4
.. questionnote::

    Напиши програм који сортира листу имена и исписује сортирану листу. (Урадити исти за листу бројева.)

.. activecode:: liste_vezba4
    :coach:

    imena = ['Marko', 'Ana', 'Jovan', 'Mira']
    
    # DOPUNI
    
    print(imena)


.. ZADATAK 5
.. questionnote::

    Напиши програм који броји колико се пута појављује одређени број у листи. Листа се састоји од `n` унетих бројева.

.. activecode:: liste_vezba5
    :coach:

    n = int(input('Unesite broј elemenata: '))
    brojevi = []
    
    # DOPUNI: Učitavanje n brojeva u listu
    
    broj_za_prebrojavanje = int(input('Unesite broj za prebrojavanje: '))

    # DOPUNI: Prebrojavanje broja u listi

    print("Broj se pojavljuje", broj_pojavljivanja, "puta.")

.. infonote::

    Да би се унели бројеви у листу, потребно је да се користи петља која ће учитати све бројеве које корисник унесе.
    Учитане бројеве треба надовезати на листу користећи метод `append`.

.. learnmorenote::

    Напредни начин решавања

    За решавање овог задатка могуће је користити функцију `count` која броји колико пута се одређени елемент појављује у листи:

    .. code-block:: python

        broj_pojavljivanja = brojevi.count(broj_za_prebrojavanje)



.. ZADATAK 6
.. questionnote::

    Напиши програм који проверава да ли се одређени елемент налази у листи.

.. activecode:: liste_vezba6
    :coach:

    imena = ['Marko', 'Ana', 'Jovan', 'Mira']
    
    # DOPUNI
    
    print('Ana јe u listi:', provera)

.. learnmorenote::

    Напредни начин решавања

    За решавање овог задатка могуће је користити оператор `in` који проверава да ли се елемент налази у листи:

    .. code-block:: python

        provera = 'Ana' in imena

    Овај израз враћа `True` ако се елемент налази у листи и `False` ако се не налази.


.. ZADATAK 7
.. questionnote::

    Креирај листу са бројевима која садржи дупликате. Напиши програм који уклања дупликате и исписује нову листу.

.. activecode:: liste_vezba7
    :coach:

    brojevi = [1, 2, 2, 3, 4, 4, 5]

    # DOPUNI
    
    print(nova_lista)

.. learnmorenote::

    Напредни начин решавања

    За решавање овог задатка могуће је користити функционалност провере да ли се елемент налази у листи.
    Ова функционалност враћа `True` ако се елемент налази у листи и `False` ако се не налази.

    .. code-block:: python

        nova_lista = []
        for broj in brojevi:
            if broj not in nova_lista:
                nova_lista.append(broj)
    

.. learnmorenote::

    Напредни начин решавања користећи скуп

    За решавање овог задатка могуће је користити функцију `set` која креира скуп од листе. Скуп је структура података која не дозвољава дупликате.

    .. code-block:: python

        nova_lista = list(set(brojevi))

    У овом примеру листу претварамо у скуп и тиме аутоматски бришемо дупликате јер унутар скупа не постоје дупликати, а након тога 
    скуп претварамо у листу како би добили листу без дупликата.



.. ZADATAK 8
.. questionnote::

    Напиши програм који преокреће редослед елемената у листи.

.. activecode:: liste_vezba8
    :coach:

    brojevi = [1, 2, 3, 4, 5]
    preokrenuta_lista = []

    # DOPUNI
    
    print(preokrenuta_lista)


.. learnmorenote::

    Напредни начин решавања

    За решавање овог задатка могуће је користити функцију `reverse` која преокреће редослед елемената у листи:

    .. code-block:: python

        brojevi.reverse()

    Ова функција мења листу у месту, што значи да не враћа нову листу већ мења постојећу.



.. ZADATAK 9
.. questionnote::

    Креирај листу бројева и филтрирај само оне који су већи од 10.

.. activecode:: liste_vezba9
    :coach:

    brojevi = [5, 12, 18, 3, 7, 22, 15]
    filtrirani_brojevi = []

    for broj in brojevi:
        # DOPUNI
    
    print(filtrirani_brojevi)



.. ZADATAK 10
.. questionnote::

    Креирај листу бројева и пронађи максимални и минимални број.

.. activecode:: liste_vezba10
    :coach:

    brojevi = [10, 20, 30, 5, 40]

    # DOPUNI
    
    print('Maksimalni broј:', maksimalni)
    print('Minimalni broј:', minimalni)

.. infonote::

    За решавање овог задатка могуће је користити функције `max` и `min` које враћају максимални и минимални елемент листе.

    .. code-block:: python

        maksimalni = max(brojevi)
        minimalni = min(brojevi)

    Пробај да решиш задатак без коришћења ових функција.

.. ZADATAK 11
.. questionnote::

    Напиши програм који прави копију постојеће листе и мења копију.

.. activecode:: liste_vezba11
    :coach:

    boje = ['crvena', 'plava', 'zelena']

    nova_lista = # DOPUNI
    nova_lista.append('žuta')

    print('Originalna lista:', boje)
    print('Kopirana lista:', nova_lista)

.. infonote::

    Ако се `nova_lista` одреди само као `nova_lista = boje`, обе листе ће показивати на исти објекат у меморији 
    и промене на једној листи ће се одразити и на другој (испробај). Да би се креирала копија листе, потребно је користити 
    метод `copy()`.


.. ZADATAK 12
.. questionnote::

    Креирај листу бројева и израчунај збир свих елемената. Листа се уноси елемент по елемент. 
    Ако је унета реч 'kraj', програм треба да се заврши са уносом.

.. activecode:: liste_vezba12
    :coach:

    # DOPUNI: Ulaz

    # DOPUNI: Izračunavanje zbira

    print('Zbir svih brojeva je:', zbir)


.. ZADATAK 14
.. questionnote::

    Креирај листу речи и испиши прво слово сваке речи.

.. activecode:: liste_vezba14
    :coach:

    reci = ['Marko', 'Ana', 'Jovan', 'Mira']
    
    for rec in reci:
        # DOPUNI

.. infonote::

    Да би се приступило првом слову речи, потребно је приступити карактеру на првом месту у стрингу који представља реч.
    Карактеру у стрингу се приступа коришћењем индекса. Први карактер у стрингу има индекс 0, други индекс 1, итд. 
    Приметићемо да су стрингови у ствари само листе карактера (стрингови имају додатне функције и методе које су посебно прављене 
    за стрингове, али у основи јесу само листе карактера).

