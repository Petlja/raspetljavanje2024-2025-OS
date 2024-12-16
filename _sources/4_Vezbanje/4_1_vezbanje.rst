Вежбање
========

.. infonote::

    Поента овог програма је да вам понуди прилику да научите што више о основама програмирања у Пајтону. Размишљајући о томе, фокусирајте се да извучете све што можете из сваког задатка, тако што ћете осигурати да задатак у целости разумете. Сасвим је у реду да један задатак радите дуже него што сте очекивали.  Ментори су увек ту за вас да вам помогну, тако да је увек можете да затражите помоћ и додатно објашњење.  Свакако,  када тражите помоћ од ментора или их тражите на интернету, фокусирајте се да научите логику иза решења и нове концепте уместо само да урадите задатак да бисте га урадили. Укратко, **вежбе радите са идејом да стекнете што више знања а не да бисте што више вежби урадили**.


Задатак 1
-----------

Напиши програм који учитава број `n` и исписује све парне бројеве од 1 до `n`.

.. activecode:: zadatak1
    :coach:
    
    # Допуни

**Пример 1**:

**Улаз**:  
10  

**Излаз**:  
2 4 6 8 10  

**Објашњење излаза**:  
Сви парни бројеви између 1 и 10 су исписани.

**Пример 2**:

**Улаз**:  
7  

**Излаз**:  
2 4 6  

**Објашњење излаза**:  
Сви парни бројеви између 1 и 7 су исписани.

.. reveal:: 4_1_resenje_6_1_1
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        n = int(input("Унесите број: "))  # Учитавање горње границе
        for i in range(1, n + 1):         # Петља пролази кроз све бројеве од 1 до n
            if i % 2 == 0:                # Провера да ли је број паран
                print(i, end=" ")         # Испис парних бројева


Задатак 2
-----------

Напиши програм који проверава да ли је унети број прост.

.. activecode:: zadatak2
    :coach:
    
    # Допуни

**Пример 1**:

**Улаз**:  
13  

**Излаз**:  
Број 13 је прост.  

**Објашњење излаза**:  
Број 13 је дељив само са 1 и самим собом.

**Пример 2**:

**Улаз**:  
10  

**Излаз**:  
Број 10 није прост.  

**Објашњење излаза**:  
Број 10 има више делилаца осим 1 и самог себе (нпр. 2 и 5).

.. reveal:: 4_1_resenje_6_1_2
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        n = int(input("Unesite broj: "))  # Учитавање броја
        if n < 2:                         # Провера да ли је број мањи од 2
            print("Broj nije prost.")
        else:
            prost = True                  # Претпостављамо да је број прост
            for i in range(2, int(n ** 0.5) + 1):  # Пролазимо до квадратног корена броја
                if n % i == 0:             # Провера да ли постоји делилац осим 1 и n
                    prost = False
                    break
            if prost:
                print(f"Broj {n} je prost.")
            else:
                print(f"Broj {n} nije prost.")


Задатак 3
-----------

Напиши програм који рачуна факторијел унетог броја.

.. activecode:: zadatak3
    :coach:
    
    # Допуни

**Пример 1**:

**Улаз**:  
5  

**Излаз**:  
Факторијел броја 5 је 120.  

**Објашњење излаза**:  
Факторијел се рачуна као :math:`5! = 5 \times 4 \times 3 \times 2 \times 1 = 120`.

**Пример 2**:

**Улаз**:  
3  

**Излаз**:  
Факторијел броја 3 је 6.  

**Објашњење излаза**:  
Факторијел се рачуна као :math:`3! = 3 \times 2 \times 1 = 6`.

.. reveal:: 4_1_resenje_6_1_3
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        n = int(input("Unesite broj: "))  # Учитавање броја
        faktorijel = 1                   # Иницијализација факторијела
        for i in range(1, n + 1):         # Петља од 1 до n
            faktorijel *= i              # Множење тренутног броја
        print(f"Faktorijel broja {n} je {faktorijel}.")


Задатак 4
-----------

Напиши програм који проверава да ли је унети број Армстронгов број.

.. activecode:: zadatak4
    :coach:
    
    # Dopuni

**Пример 1**:

**Улаз**:  
153  

**Излаз**:  
Број 153 је Армстронгов број.  

**Објашњење излаза**:  
Цифре броја 153 подигнуте на трећи степен дају: :math:`1^3 + 5^3 + 3^3 = 1 + 125 + 27 = 153`. 

**Пример 2**:

**Улаз**:  
123  

**Излаз**:  
Број 123 није Армстронгов број.  

**Објашњење излаза**:  
Цифре броја 123 подигнуте на трећи степен дају: :math:`1^3 + 2^3 + 3^3 = 1 + 8 + 27 = 36`. 

.. infonote:: Шта је Армстронгов број?

    Армстронгов број је број који је једнак збиру својих цифара подигнутих на степен једнак броју цифара у том броју.

    **Пример:**

    - Број 153 има три цифре: (1, 5, 3).

    - Збир цифара подигнутих на трећи степен је:

    :math:`1^3 + 5^3 + 3^3 = 1 + 125 + 27 = 153`

    - Пошто је збир једнак броју 153, то је Армстронгов број.
        
    **Још примера Армстронгових бројева:**
    - 370, 371, 407 (троцифрени Армстронгови бројеви).
    - 9474 (четвороцифрени Армстронгов број).


.. reveal:: 4_1_resenje_6_1_4
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        n = int(input("Unesite broj: "))  # Учитавање броја
        suma = 0                          # Иницијализација суме цифара на степен
        broj_cifara = len(str(n))         # Број цифара у броју
        original = n                      # Чувамо оригиналну вредност броја
        while n > 0:
            cifra = n % 10                # Екстракција последње цифре
            suma += cifra ** broj_cifara  # Додавање цифре на одговарајући степен
            n //= 10                      # Уклањање последње цифре
        if suma == original:              # Провера да ли је збир једнак оригиналу
            print(f"Broj {original} je Armstrongov broj.")
        else:
            print(f"Broj {original} nije Armstrongov broj.")


Задатак 5
-----------

Напиши програм који исписује све троцифрене бројеве код којих је збир цифара једнак 10.

.. activecode:: zadatak5
    :coach:
    
    # Dopuni

**Пример 1**:

**Улаз**:  
(Нема додатног уноса, троцифрени бројеви се проверавају аутоматски.)  

**Излаз**:  
109

118

127

136

145

154

163

172

181

190

208

217

226

235

244

253

262

271

280

307

316

325

334

343

352

361

370

406

415

424

433

442

451

460

505

514

523

532

541

550

604

613

622

631

640

703

712

721

730

802

811

820

901

910

**Објашњење излаза**:  
Исписани су сви троцифрени бројеви где је збир цифара једнак 10, на пример: за 118, :math:`1 + 1 + 8 = 10`.


.. reveal:: 4_1_resenje_6_1_5
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        for broj in range(100, 1000):  # Итерација кроз све троцифрене бројеве
            cifra1 = broj // 100       # Прва цифра
            cifra2 = (broj // 10) % 10 # Друга цифра
            cifra3 = broj % 10         # Трећа цифра
            if cifra1 + cifra2 + cifra3 == 10:  # Провера да ли је збир цифара 10
                print(broj, end=" ")            # Испис бројева


Задатак 6
-----------

Напиши програм који за унети број `n` исписује све његове делиоце.

.. activecode:: zadatak6
    :coach:
    
    # Dopuni

**Пример 1**:

**Улаз**:  
12  

**Излаз**:  
1 2 3 4 6 12  

**Објашњење излаза**:  
Делиоце броја 12 чине сви бројеви који без остатка деле 12, укључујући и 12.

**Пример 2**:

**Улаз**:  
15  

**Излаз**:  
1 3 5 15  

**Објашњење излаза**:  
Делиоце броја 15 чине 1, 3, 5 и 15.

.. reveal:: 4_1_resenje_6_1_6
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        n = int(input("Unesite broj: "))  # Učitavanje broja
        for i in range(1, n + 1):         # Iteracija od 1 do n
            if n % i == 0:                # Provera da li je i delioc broja n
                print(i, end=" ")         # Ispis delilaca


Задатак 7
-----------

Напиши програм који проверава да ли је унети број палиндром.

.. activecode:: zadatak7
    :coach:
    
    # Dopuni

**Пример 1**:

**Улаз**:  
121  

**Излаз**:  
Број 121 је палиндром.  

**Објашњење излаза**:  
Број 121 се исто чита са леве и десне стране.

**Пример 2**:

**Улаз**:  
123  

**Излаз**:  
Број 123 није палиндром.  

**Објашњење излаза**:  
Број 123 се не чита исто са леве и десне стране.

.. reveal:: 4_1_resenje_6_1_7
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        broj = int(input("Unesite broj: "))  # Učitavanje broja
        originalni_broj = broj               # Čuvamo originalni broj za poređenje
        obrnut_broj = 0                      # Promenljiva za čuvanje obrnutog broja

        while broj > 0:
            cifra = broj % 10                # Uzimamo poslednju cifru broja
            obrnut_broj = obrnut_broj * 10 + cifra  # Dodajemo cifru na kraj obrnutog broja
            broj //= 10                      # Uklanjamo poslednju cifru iz broja

        if originalni_broj == obrnut_broj:   # Provera da li je broj isti kao njegov obrnuti oblik
            print("Broj je palindrom.")      # Ispis ako je broj palindrom
        else:
            print("Broj nije palindrom.")    # Ispis ako broj nije palindrom


Задатак 8
-----------

Напиши програм који исписује све троцифрене бројеве код којих је производ цифара једнак збиру цифара.

.. activecode:: zadatak8
    :coach:
    
    # Dopuni

**Пример 1**:

**Улаз**:  
(Нема додатног уноса, троцифрени бројеви се проверавају аутоматски.)  

**Излаз**:  
123

132

213

231

312

321

**Објашњење излаза**:  
За број 123, :math:`1 \times 2 \times 3 = 6`, a :math:`1 + 2 + 3 = 6`.

.. reveal:: 4_1_resenje_6_1_8
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        for broj in range(100, 1000):         # Iteracija kroz sve trocifrene brojeve
            cifra1 = broj // 100              # Prva cifra
            cifra2 = (broj // 10) % 10        # Druga cifra
            cifra3 = broj % 10                # Treća cifra
            proizvod = cifra1 * cifra2 * cifra3  # Proizvod cifara
            zbir = cifra1 + cifra2 + cifra3      # Zbir cifara
            if proizvod == zbir:              # Provera da li su proizvod i zbir jednaki
                print(broj, end=" ")          # Ispis brojeva


Задатак 9
-----------

Напиши програм који за унети број `n` проверава да ли је савршен број.  
(Савршен број је број једнак збиру својих правих делилаца, осим себе.)

.. activecode:: zadatak9
    :coach:
    
    # Dopuni

**Пример 1**:

**Улаз**:  
6  

**Излаз**:  
Број 6 је савршен број.  

**Објашњење излаза**:  
Прави делиоци броја 6 су 1, 2 и 3. Њихов збир :math:`1 + 2 + 3 = 6`, што значи да је 6 савршен број.

**Пример 2**:

**Улаз**:  
8  

**Излаз**:  
Број 8 није савршен број.  

**Објашњење излаза**:  
Прави делиоци броја 8 су 1, 2 и 4. Њихов збир :math:`1 + 2 + 4 = 7`, што значи да 8 није савршен број.

.. reveal:: 4_1_resenje_6_1_9
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        n = int(input("Unesite broj: "))  # Učitavanje broja
        zbir = 0                          # Inicijalizacija zbira pravih delilaca
        for i in range(1, n):             # Provera svih brojeva manjih od n
            if n % i == 0:                # Provera da li je i delioc broja n
                zbir += i                 # Dodavanje delilaca u zbir
        if zbir == n:                     # Provera da li je zbir jednak originalnom broju
            print(f"Broj {n} je savršen broj.")
        else:
            print(f"Broj {n} nije savršen broj.")


Задатак 10
-----------

Напиши програм који исписује све четвороцифрене бројеве где се свака цифра појављује тачно једном.

.. activecode:: zadatak10
    :coach:
    
    # Dopuni

**Пример 1**:

**Улаз**:  
(Нема додатног уноса, четвороцифрени бројеви се проверавају аутоматски.)  

**Излаз**:  
1023 1032 1203 1230 ...  

**Објашњење излаза**:  
Бројеви попут 1023 имају цифре 1, 0, 2 и 3 које су све различите и појављују се само једном.

.. reveal:: 4_1_resenje_6_1_10
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Prolazak kroz sve četvorocifrene brojeve
        for broj in range(1000, 10000):  
            # Izdvajanje cifara broja
            hiljade = broj // 1000
            stotine = (broj // 100) % 10
            desetice = (broj // 10) % 10
            jedinice = broj % 10

            # Provera da li su sve cifre različite
            if (hiljade != stotine and hiljade != desetice and hiljade != jedinice and
                stotine != desetice and stotine != jedinice and
                desetice != jedinice):
                print(broj)



Задатак 11
-----------

Напиши програм који за унети број исписује колико има цифара.

.. activecode:: zadatak11
    :coach:
    
    # Dopuni

**Пример 1**:

**Улаз**:  
12345  

**Излаз**:  
Број 12345 има 5 цифара.  

**Објашњење излаза**:  
Број 12345 има укупно 5 цифара, што се добија итеративним бројањем.

**Пример 2**:

**Улаз**:  
100  

**Излаз**:  
Број 100 има 3 цифре.  

**Објашњење излаза**:  
Број 100 садржи укупно 3 цифре.

.. reveal:: 4_1_resenje_6_1_11
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        broj = int(input("Unesite broj: "))  # Učitavanje broja
        brojac = 0                           # Inicijalizacija brojača cifara
        while broj != 0:                     # Petlja traje dok ima cifara u broju
            broj //= 10                      # Uklanja poslednju cifru
            brojac += 1                      # Uvećava brojač cifara
        print("Broj ima", brojac, "cifara.")  # Ispis rezultata


Задатак 12
-----------

Напиши програм који исписује све бројеве између 100 и 200 који имају бар две исте цифре.

.. activecode:: zadatak12
    :coach:
    
    # Dopuni

**Пример 1**:

**Улаз**:  
(Нема додатног уноса, анализирају се бројеви између 100 и 200.)  

**Излаз**:  
101 110 111 112 113 ...  

**Објашњење излаза**:  
Бројеви попут 101 имају две исте цифре (1 се понавља), док број 123 нема.

.. reveal:: 4_1_resenje_6_1_12
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        for broj in range(100, 200):       # Iteracija kroz brojeve od 100 do 200
            cifra1 = broj // 100           # Prva cifra
            cifra2 = (broj // 10) % 10     # Druga cifra
            cifra3 = broj % 10             # Treća cifra
            if (cifra1 == cifra2 or cifra1 == cifra3 or cifra2 == cifra3):  # Provera jednakosti cifara
                print(broj, end=" ")       # Ispis brojeva


Задатак 13
-----------

Напиши програм који рачуна најмањи и највећи број од унетих 5 бројева.

.. activecode:: zadatak13
    :coach:
    
    # Dopuni

**Пример 1**:

**Улаз**:  
5 10 15 2 8  

**Излаз**:  
Најмањи број је 2, а највећи број је 15.  

**Објашњење излаза**:  
Међу унетим бројевима, 2 је најмањи, а 15 највећи.

**Пример 2**:

**Улаз**:  
50 40 30 20 10  

**Излаз**:  
Најмањи број је 10, а највећи број је 50.  

**Објашњење излаза**:  
Бројеви су већ сортирани, али програм рачуна минимум и максимум.

.. reveal:: 4_1_resenje_6_1_13
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        prvi_broj = int(input("Unesite broj: "))  # Učitavanje prvog broja
        najmanji = prvi_broj         # Inicijalizacija najmanjeg broja na prvi broj
        najveci = prvi_broj         # Inicijalizacija najvećeg broja na prvi broj
        for _ in range(4):              # Iteracija za unos 5 brojeva
            broj = int(input("Unesite broj: "))
            if broj < najmanji:         # Provera za najmanji broj
                najmanji = broj
            if broj > najveci:          # Provera za najveći broj
                najveci = broj
        print(f"Najmanji broj je {najmanji}, a najveći broj je {najveci}.")  # Ispis rezultata


Задатак 14
-----------

Напиши програм који проверава да ли су унети бројеви у растућем поретку.

.. activecode:: zadatak14
    :coach:
    
    # Dopuni

**Пример 1**:

**Улаз**:  
1 2 3 4 5  

**Излаз**:  
Бројеви су у растућем поретку.  

**Објашњење излаза**:  
Сваки наредни број је већи од претходног, што значи да су у растућем поретку.

**Пример 2**:

**Улаз**:  
1 3 2 4 5  

**Излаз**:  
Бројеви нису у растућем поретку.  

**Објашњење излаза**:  
Број 2 није већи од броја 3, што прекида растући поредак.

.. reveal:: 4_1_resenje_6_1_14
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        prethodni = int(input("Unesite prvi broj: "))  # Učitavanje prvog broja
        rastuci = True                                 # Pretpostavljamo da je poredak rastući
        for _ in range(4):                            # Petlja za unos narednih 4 brojeva
            trenutni = int(input("Unesite sledeći broj: "))
            if trenutni <= prethodni:                 # Provera da li je trenutni broj manji ili jednak prethodnom
                rastuci = False                       # Ako nije rastući, prekida se uslov
            prethodni = trenutni                      # Ažurira prethodni broj
        if rastuci:
            print("Brojevi su u rastućem poretku.")    # Ispis ako su rastući
        else:
            print("Brojevi nisu u rastućem poretku.")  # Ispis ako nisu rastući


Задатак 15
-----------

Напиши програм који исписује све бројеве између унета два броја који су прости.

.. activecode:: zadatak15
    :coach:
    
    # Dopuni

**Пример 1**:

**Улаз**:  
10  
20  

**Излаз**:  
11 13 17 19  

**Објашњење излаза**:  
У опсегу од 10 до 20 прости бројеви су они који су дељиви само са 1 и са самим собом.

**Пример 2**:

**Улаз**:  
5  
15  

**Излаз**:  
5 7 11 13  

**Објашњење излаза**:  
У опсегу од 5 до 15, прости бројеви су 5, 7, 11 и 13.

.. reveal:: 4_1_resenje_6_1_15
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        donja_granica = int(input("Unesite donju granicu: "))   # Učitavanje donje granice
        gornja_granica = int(input("Unesite gornju granicu: ")) # Učitavanje gornje granice
        for broj in range(donja_granica, gornja_granica + 1):  # Iteracija kroz opseg
            prost = True                                       # Pretpostavljamo da je broj prost
            if broj > 1:                                       # Broj mora biti veći od 1 da bi bio prost
                for i in range(2, int(broj**0.5) + 1):         # Provera delilaca do kvadratnog korena
                    if broj % i == 0:
                        prost = False                          # Ako je deljiv, nije prost
                        break
                if prost:
                    print(broj, end=" ")                       # Ispis prostog broja


Задатак 16
-----------

Напиши програм који исписује све бројеве од 1 до унетог броја који имају тачно 3 делиоца.

.. activecode:: zadatak16
    :coach:
    
    # Dopuni

**Пример 1**:

**Улаз**:  
20  

**Излаз**:  
4 9 16  

**Објашњење излаза**:  
Бројеви 4, 9 и 16 су квадрати простих бројева и имају тачно 3 делиоца.

**Пример 2**:

**Улаз**:  
30  

**Излаз**:  
4 9 16 25  

**Објашњење излаза**:  
Додаје се 25, јер је и он квадрат простог броја.

.. reveal:: 4_1_resenje_6_1_16
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        n = int(input("Unesite broj: "))          # Učitavanje broja
        for broj in range(1, n + 1):             # Iteracija kroz brojeve do n
            delioci = 0                          # Brojač delilaca
            for i in range(1, broj + 1):         # Provera svih potencijalnih delilaca
                if broj % i == 0:
                    delioci += 1                # Uvećanje broja delilaca
            if delioci == 3:                    # Provera da li broj ima tačno 3 delioca
                print(broj, end=" ")            # Ispis brojeva


Задатак 17
-----------

Напиши програм који проверава да ли се унети бројеви мењају између парних и непарних.

.. activecode:: zadatak17
    :coach:
    
    # Dopuni

**Пример 1**:

**Улаз**:  
1 2 8 4 5  

**Излаз**:  
Бројеви се не мењају између парних и непарних.  

**Објашњење излаза**:  
Парни и непарни бројеви се не смењују редом, већ долазе у групама.

**Пример 2**:

**Улаз**:  
1 2 3 4 3 2  

**Излаз**:  
Бројеви се мењају између парних и непарних.  

**Објашњење излаза**:  
Сваки наредни број мења парност.

.. reveal:: 4_1_resenje_6_1_17
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        prethodni = int(input("Unesite prvi broj: "))  # Učitavanje prvog broja
        smenjuju_se = True                            # Pretpostavka da se smenjuju
        for _ in range(4):                            # Petlja za unos 4 naredna broja
            trenutni = int(input("Unesite sledeći broj: "))
            if (prethodni % 2 == trenutni % 2):       # Provera iste parnosti
                smenjuju_se = False                  # Ako su iste parnosti, prekid uslova
            prethodni = trenutni                     # Ažuriranje prethodnog broja
        if smenjuju_se:
            print("Brojevi se menjaju između parnih i neparnih.")  # Ispis ako se smenjuju
        else:
            print("Brojevi se ne menjaju između parnih i neparnih.")  # Ispis ako se ne smenjuju


Задатак 18
-----------

Напиши програм који за унети број исписује да ли има све јединствене цифре.


.. activecode:: zadatak18
    :coach:
    
    # Dopuni

**Пример 1**:

**Улаз**:  
12345  

**Излаз**:  
Број 12345 има све јединствене цифре.  

**Објашњење излаза**:  
Свака цифра у броју 12345 појављује се тачно једном.

**Пример 2**:

**Улаз**:  
11234  

**Излаз**:  
Број 11234 нема све јединствене цифре.  

**Објашњење излаза**:  
Цифра 1 појављује се два пута.

.. reveal:: 4_1_resenje_6_1_18
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Unos broja od korisnika
        broj = int(input("Unesite broj: "))

        # Kopija broja za izdvajanje cifara
        originalni_broj = broj
        jedinstvene = True

        # Provera svake cifre sa svim ostalim ciframa
        while broj > 0:
            trenutna_cifra = broj % 10
            privremeni_broj = originalni_broj // 10  # Počinje nakon trenutne cifre

            while privremeni_broj > 0:
                poredna_cifra = privremeni_broj % 10
                if trenutna_cifra == poredna_cifra:
                    jedinstvene = False
                    break
                privremeni_broj //= 10

            if not jedinstvene:
                break

            broj //= 10

        # Ispis rezultata
        if jedinstvene:
            print("Broj ima sve jedinstvene cifre.")+
        else:
            print("Broj nema sve jedinstvene cifre.")

