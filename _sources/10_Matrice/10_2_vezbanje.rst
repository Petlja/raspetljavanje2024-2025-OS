Вежбање
========


Задатак 1
---------

Напиши програм који креира матрицу димензије 3x3 и попуњава је нулама. Прикажи резултат.

.. activecode:: v20_zadatak1
    :coach:

    # Kreiraj praznu matricu(listu)

    for i in range(3):
        # Kreiraj praznu listu
        
        for j in range(3):
            # Додавање нуле у ред
    
        # Додавање реда у матрицу

    # Приказ матрице
    for # Dopuni
        for # Dopuni
            print(element, end=" ")
        print()

        
**Пример 1**:

**Улаз**:  
Нема уноса.

**Излаз**:  

0 0 0  

0 0 0  

0 0 0  

.. reveal:: 20_1_resenje_20_1_1
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Креирање матрице 3x3 попуњене нулама
        matrix = []
        for i in range(3):
            row = []  # Креирање новог реда
            for j in range(3):
                row.append(0)  # Додавање нуле у ред
            matrix.append(row)  # Додавање реда у матрицу

        # Приказ матрице
        for row in matrix:
            for element in row:
                print(element, end=" ")
            print()

Задатак 2
---------

Напиши програм који омогућава кориснику да унесе елементе матрице димензије 2x2.

.. activecode:: v20_zadatak2
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  

1 2  

3 4  

**Излаз**:  

1 2  

3 4  

**Пример 2**:

**Улаз**:  

5 6  

7 8  

**Излаз**:  

5 6  

7 8  

.. reveal:: 20_2_resenje_20_2_1
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос елемената матрице 2x2
        matrix = []
        print("Унесите елементе матрице 2x2 (раздвојене размацима):")
        for i in range(2):
            row = []  # Креирање новог реда
            elements = (input("Унесите елементе за ред", i + 1 , ": ").split())
            for elem in elements:
                row.append(int(elem))  # Додавање елемента у ред
            matrix.append(row)  # Додавање реда у матрицу

        # Приказ матрице
        for row in matrix:
            for element in row:
                print(element, end=" ")
            print()

Задатак 3
---------

Напиши програм који уноси матрицу и рачуна суму свих елемената матрице димензије 3x3.

.. activecode:: v20_zadatak3
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  

1 2 3  

4 5 6  

7 8 9  

**Излаз**:  

45  

**Пример 2**:

**Улаз**:  

2 4 6  

8 10 12  

14 16 18  

**Излаз**:  

90  


.. reveal:: 20_3_resenje_20_3_1
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос елемената матрице 3x3
        matrix = []
        print("Унесите елементе матрице 3x3 (раздвојене размацима):")
        for i in range(3):
            row = []  # Креирање новог реда
            elements = input("Унесите елементе за ред", i + 1 , ": ").split()
            for elem in elements:
                row.append(int(elem))  # Додавање елемента у ред
            matrix.append(row)  # Додавање реда у матрицу

        # Израчунавање суме елемената
        total_sum = 0
        for row in matrix:
            for element in row:
                total_sum += element  # Додавање елемента у суму

        # Испис резултата
        print("Сума свих елемената је:", total_sum)

Задатак 4
---------

Напиши програм који проналази и исписује елементе главне дијагонале матрице димензије 3x3.

.. activecode:: v20_zadatak4
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  

1 2 3  

4 5 6  

7 8 9  

**Излаз**:  

1 5 9  

**Пример 2**:

**Улаз**:  

2 4 6  

8 10 12  

14 16 18  

**Излаз**:  

2 10 18  

.. reveal:: 20_4_resenje_20_4_1
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос елемената матрице 3x3
        matrix = []
        print("Унесите елементе матрице 3x3 (раздвојене размацима):")
        for i in range(3):
            row = []  # Креирање новог реда
            elements = input("Унесите елементе за ред", i + 1 , ": ").split()
            for elem in elements:
                row.append(int(elem))  # Додавање елемента у ред
            matrix.append(row)  # Додавање реда у матрицу

        # Проналажење елемената главне дијагонале
        diagonal_elements = []
        for i in range(3):
            diagonal_elements.append(matrix[i][i])  # Додавање елемента дијагонале

        # Испис дијагоналних елемената
        print("Елементи главне дијагонале су:")
        for element in diagonal_elements:
            print(element)


Задатак 5
---------

Напиши програм који проверава да ли је квадратна матрица симетрична.  
**Симетрична матрица** је квадратна матрица где је `a[i][j] == a[j][i]` за све валидне индексе.

.. activecode:: v20_zadatak5
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  

1 2 3  

2 4 5  

3 5 6  

**Излаз**:  

True  

**Пример 2**:

**Улаз**:  

1 0 0  

0 1 1  

0 1 1  

**Излаз**:  

False  

.. reveal:: 20_5_resenje_20_5_1
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос елемената квадратне матрице
        matrix = []
        n = int(input("Унесите димензију квадратне матрице (n): "))
        print("Унесите елементе матрице (раздвојене размацима):")
        for i in range(n):
            row = []
            elements = input("Унесите елементе за ред", i + 1": ").split()
            for elem in elements:
                row.append(int(elem))
            matrix.append(row)

        # Провера симетричности
        is_symmetric = True
        for i in range(n):
            for j in range(n):
                if matrix[i][j] != matrix[j][i]:
                    is_symmetric = False
                    break

        # Испис резултата
        if is_symmetric:
            print("True")
        else:
            print("False")

Задатак 6
---------

Напиши програм који сабира две матрице димензије 3x3.

.. activecode:: v20_zadatak6
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  
Прва матрица:  

1 2 3  

4 5 6  

7 8 9  

Друга матрица:  

9 8 7  

6 5 4  

3 2 1  

**Излаз**:  

10 10 10  

10 10 10  

10 10 10  

**Пример 2**:

**Улаз**:  

Прва матрица:  

0 0 0  

0 0 0  

0 0 0  

Друга матрица:  

1 2 3  

4 5 6  

7 8 9  

**Излаз**:  

1 2 3  

4 5 6  

7 8 9  

.. reveal:: 20_6_resenje_20_6_1
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос две матрице
        def input_matrix(size):
            matrix = []
            for i in range(size):
                row = []
                elements = input("Унесите елементе за ред", i + 1": ").split()
                for elem in elements:
                    row.append(int(elem))
                matrix.append(row)
            return matrix

        print("Унос прве матрице 3x3:")
        matrix1 = input_matrix(3)

        print("Унос друге матрице 3x3:")
        matrix2 = input_matrix(3)

        # Сабирање матрица
        result = []
        for i in range(3):
            row = []
            for j in range(3):
                row.append(matrix1[i][j] + matrix2[i][j])
            result.append(row)

        # Испис резултата
        print("Резултат сабирања:")
        for row in result:
            for element in row:
                print(element, end=" ")
            print()

Задатак 7
---------

Напиши програм који проверава да ли је дата квадратна јединична матрица (или матрица идентитета - *identity matrix*).  
**Јединична матрица** има све елементе на дијагонали једнаке 1, а остале 0. На улазу, уноси се матрица димензија *m*x*n*.

.. activecode:: v20_zadatak7
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  

1 0 0  

0 1 0  

0 0 1  

**Излаз**:  
True  

**Пример 2**:

**Улаз**:  

1 0 1  

0 1 0  

0 0 1  

**Излаз**:  
False  

.. reveal:: 20_7_resenje_20_7_1
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос елемената квадратне матрице
        matrix = []
        n = int(input("Унесите димензију квадратне матрице (n): "))
        print("Унесите елементе матрице (раздвојене размацима):")
        for i in range(n):
            row = []
            elements = input("Унесите елементе за ред", i + 1": ").split()
            for elem in elements:
                row.append(int(elem))
            matrix.append(row)

        # Провера идентичности
        is_identity = True
        for i in range(n):
            for j in range(n):
                if i == j and matrix[i][j] != 1:
                    is_identity = False
                elif i != j and matrix[i][j] != 0:
                    is_identity = False

        # Испис резултата
        if is_identity:
            print("True")
        else:
            print("False")

Задатак 8
---------

Напиши програм који множи све елементе матрице са задатим скаларним бројем (нпр. 3). На улазу, уноси се матрица димензија *m*x*n*. Резултат прикажи као нову матрицу. 

.. activecode:: v20_zadatak8
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  
Матрица:  

1 2 3  

4 5 6  

7 8 9  

Скалaр: 2  

**Излаз**:  

2 4 6  

8 10 12  

14 16 18  

**Пример 2**:

**Улаз**:  
Матрица:  

1 0 0  

0 1 0  

0 0 1  

Скалaр: 3  

**Излаз**:  

3 0 0  

0 3 0  

0 0 3  

.. reveal:: 20_8_resenje_20_8_1
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос матрице и скалара
        matrix = []
        print("Унесите елементе матрице 3x3 (раздвојене размацима):")
        for i in range(3):
            row = []
            elements = input("Унесите елементе за ред", i + 1": ").split()
            for elem in elements:
                row.append(int(elem))
            matrix.append(row)

        scalar = int(input("Унесите скалар: "))

        # Множење матрице са скаларом
        result = []
        for i in range(3):
            row = []
            for j in range(3):
                row.append(matrix[i][j] * scalar)
            result.append(row)

        # Испис резултата
        print("Резултат множења:")
        for row in result:
            for element in row:
                print(element, end=" ")
            print()


Задатак 9
---------

Напиши програм који ротира дату квадратну матрицу за 90 степени удесно. На улазу, уноси се матрица димензија *m*x*n*. Резултат прикажи као нову матрицу.

.. activecode:: v20_zadatak9
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  

1 2 3  

4 5 6  

7 8 9  

**Излаз**:  

7 4 1  

8 5 2  

9 6 3  

**Пример 2**:

**Улаз**:  

1 0 0  

0 1 0  

0 0 1  

**Излаз**:  

0 0 1  

0 1 0  

1 0 0  

.. reveal:: 20_9_resenje_20_9_1
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос квадратне матрице
        matrix = []
        n = int(input("Унесите димензију квадратне матрице (n): "))
        print("Унесите елементе матрице (раздвојене размацима):")
        for i in range(n):
            row = []
            elements = input("Унесите елементе за ред", i + 1": ").split()
            for elem in elements:
                row.append(int(elem))
            matrix.append(row)

        # Ротација матрице за 90 степени удесно
        rotated_matrix = []
        for i in range(n):
            new_row = []
            for j in range(n):
                new_row.append(matrix[n - j - 1][i])
            rotated_matrix.append(new_row)

        # Испис резултата
        print("Ротирана матрица:")
        for row in rotated_matrix:
            for element in row:
                print(element, end=" ")
            print()

Задатак 10
----------

Напиши програм који проверава да ли је дата квадратна матрица дијагонална.  
**Дијагонална матрица** има све елементе ван главне дијагонале једнаке 0. На улазу, уноси се матрица димензија *m*x*n*. 

.. activecode:: v20_zadatak10
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  

1 0 0  

0 2 0  

0 0 3  

**Излаз**:  
True  

**Пример 2**:

**Улаз**:  

1 0 1  

0 2 0  

0 0 3  

**Излаз**:  
False  

.. reveal:: 20_10_resenje_20_10_1
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос квадратне матрице
        matrix = []
        n = int(input("Унесите димензију квадратне матрице (n): "))
        print("Унесите елементе матрице (раздвојене размацима):")
        for i in range(n):
            row = []
            elements = input("Унесите елементе за ред", i + 1": ").split()
            for elem in elements:
                row.append(int(elem))
            matrix.append(row)

        # Провера да ли је матрица дијагонална
        is_diagonal = True
        for i in range(n):
            for j in range(n):
                if i != j and matrix[i][j] != 0:
                    is_diagonal = False
                    break

        # Испис резултата
        if is_diagonal:
            print("True")
        else:
            print("False")

Задатак 11
----------

Напиши програм који проверава да ли је дата квадратна матрица горњетроугаона.  
**Горњетроугаона матрица** има све елементе испод главне дијагонале једнаке 0. На улазу, уноси се матрица димензија *m*x*n*. 

.. activecode:: v20_zadatak11
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  

1 2 3  

0 4 5  

0 0 6  

**Излаз**:  
True  

**Пример 2**:

**Улаз**:  

1 2 3  

4 5 6  

7 8 9  

**Излаз**:  
False  

.. reveal:: 20_11_resenje_20_11_1
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос квадратне матрице
        matrix = []
        n = int(input("Унесите димензију квадратне матрице (n): "))
        print("Унесите елементе матрице (раздвојене размацима):")
        for i in range(n):
            row = []
            elements = input("Унесите елементе за ред", i + 1": ").split()
            for elem in elements:
                row.append(int(elem))
            matrix.append(row)

        # Провера да ли је матрица горњетроугаона
        is_upper_triangular = True
        for i in range(n):
            for j in range(i):
                if matrix[i][j] != 0:
                    is_upper_triangular = False
                    break

        # Испис резултата
        if is_upper_triangular:
            print("True")
        else:
            print("False")

Задатак 12
----------

Напиши програм који проналази највећи елемент у сваком реду матрице и исписује резултат. На улазу, уноси се матрица димензија *m*x*n*. 

.. activecode:: v20_zadatak12
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  

1 2 3  

4 5 6  

7 8 9  

**Излаз**:  

3  

6  

9  

**Пример 2**:

**Улаз**:  

10 20 30  

5 15 25  

1 2 3  

**Излаз**:  

30  

25  

3  

.. reveal:: 20_12_resenje_20_12_1
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос елемената матрице
        matrix = []
        m = int(input("Унесите број редова (m): "))
        n = int(input("Унесите број колона (n): "))
        print("Унесите елементе матрице (раздвојене размацима):")
        for i in range(m):
            row = []
            elements = input("Унесите елементе за ред", i + 1": ").split()
            for elem in elements:
                row.append(int(elem))
            matrix.append(row)

        # Проналажење највећег елемента у сваком реду
        print("Највећи елементи у редовима су:")
        for row in matrix:
            max_element = row[0]
            for element in row:
                if element > max_element:
                    max_element = element
            print(max_element)


Задатак 13
----------

Напиши програм који замењује први и последњи ред у задатој матрици. На улазу, уноси се матрица димензија *m*x*n*. 

.. activecode:: v20_zadatak13
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  

1 2 3  

4 5 6  

7 8 9  

**Излаз**:  

7 8 9  

4 5 6  

1 2 3  

**Пример 2**:

**Улаз**:  

10 20 30  

40 50 60  

70 80 90  

**Излаз**:  

70 80 90  

40 50 60  

10 20 30  

.. reveal:: 20_13_resenje_20_13_1
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос елемената матрице
        matrix = []
        m = int(input("Унесите број редова (m): "))
        n = int(input("Унесите број колона (n): "))
        print("Унесите елементе матрице (раздвојене размацима):")
        for i in range(m):
            row = []
            elements = input("Унесите елементе за ред", i + 1": ").split()
            for elem in elements:
                row.append(int(elem))
            matrix.append(row)

        # Замена првог и последњег реда
        matrix[0], matrix[-1] = matrix[-1], matrix[0]

        # Испис резултата
        print("Модификована матрица:")
        for row in matrix:
            for element in row:
                print(element, end=" ")
            print()

Задатак 14
----------

Напиши програм који обрће редослед елемената у сваком реду матрице. На улазу, уноси се матрица димензија *m*x*n*. 

.. activecode:: v20_zadatak14
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  

1 2 3  

4 5 6  

7 8 9  

**Излаз**:  

3 2 1  

6 5 4  

9 8 7  

**Пример 2**:

**Улаз**:  

10 20 30  

40 50 60  

70 80 90  

**Излаз**:  

30 20 10  

60 50 40  

90 80 70  

.. reveal:: 20_14_resenje_20_14_1
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос елемената матрице
        matrix = []
        m = int(input("Унесите број редова (m): "))
        n = int(input("Унесите број колона (n): "))
        print("Унесите елементе матрице (раздвојене размацима):")
        for i in range(m):
            row = []
            elements = input("Унесите елементе за ред", i + 1": ").split()
            for elem in elements:
                row.append(int(elem))
            matrix.append(row)

        # Обртање редоследа елемената у сваком реду
        for i in range(m):
            matrix[i] = matrix[i][::-1]

        # Испис резултата
        print("Модификована матрица:")
        for row in matrix:
            for element in row:
                print(element, end=" ")
            print()

Задатак 15
----------

Напиши програм који обрће редослед редова у матрици (последњи ред постаје први, итд). На улазу, уноси се матрица димензија *m*x*n*. 

.. activecode:: v20_zadatak15
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  

1 2 3  

4 5 6  

7 8 9  

**Излаз**:  

7 8 9  

4 5 6  

1 2 3  

**Пример 2**:

**Улаз**:  

10 20 30  

40 50 60  

70 80 90  

**Излаз**:  

70 80 90  

40 50 60  

10 20 30  

.. reveal:: 20_15_resenje_20_15_1
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос елемената матрице
        matrix = []
        m = int(input("Унесите број редова (m): "))
        n = int(input("Унесите број колона (n): "))
        print("Унесите елементе матрице (раздвојене размацима):")
        for i in range(m):
            row = []
            elements = input("Унесите елементе за ред", i + 1": ").split()
            for elem in elements:
                row.append(int(elem))
            matrix.append(row)

        # Обртање редоследа редова у матрици
        matrix.reverse()

        # Испис резултата
        print("Модификована матрица:")
        for row in matrix:
            for element in row:
                print(element, end=" ")
            print()

Задатак 16
----------

Напиши програм који додаје нови ред на крај матрице. Корисник уноси елементе новог реда. На улазу, уноси се матрица димензија *m*x*n*. 

.. activecode:: v20_zadatak16
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  
Матрица:  

1 2 3  

4 5 6  

Нови ред: 7 8 9  

**Излаз**:  

1 2 3  

4 5 6  

7 8 9  

**Пример 2**:

**Улаз**:  
Матрица:  

10 20 30  

40 50 60  

Нови ред: 70 80 90  

**Излаз**:  

10 20 30  

40 50 60  

70 80 90  

.. reveal:: 20_16_resenje_20_16_1
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос елемената матрице
        matrix = []
        m = int(input("Унесите број редова (m): "))
        n = int(input("Унесите број колона (n): "))
        print("Унесите елементе матрице (раздвојене размацима):")
        for i in range(m):
            row = []
            elements = input("Унесите елементе за ред", i + 1": ").split()
            for elem in elements:
                row.append(int(elem))
            matrix.append(row)

        # Додавање новог реда
        print("Унесите елементе новог реда (раздвојене размацима):")
        new_row = []
        elements = input("Елементи новог реда: ").split()
        for elem in elements:
            new_row.append(int(elem))
        matrix.append(new_row)

        # Испис резултата
        print("Модификована матрица:")
        for row in matrix:
            for element in row:
                print(element, end=" ")
            print()


Задатак 17
-----------

Напиши програм који прво уноси бројеве *m* и *n*, а затим уноси матрицу димензија *m × n* и исписује је.

.. activecode:: v20_zadatak17
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  

m: 2  

n: 3  

Матрица:  

1 2 3  

4 5 6  

**Излаз**:  

1 2 3  

4 5 6  

**Пример 2**:

**Улаз**:  

m: 3  

n: 2  

Матрица:  

7 8  

9 10  

11 12  

**Излаз**:  

7 8  

9 10  

11 12  

.. reveal:: 20_17_resenje_20_17_1
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос димензија матрице
        m = int(input("Унесите број редова (m): "))
        n = int(input("Унесите број колона (n): "))

        # Унос елемената матрице
        matrix = []
        print("Унесите елементе матрице (раздвојене размацима):")
        for i in range(m):
            row = []
            elements = input("Унесите елементе за ред", i + 1": ").split()
            for elem in elements:
                row.append(int(elem))
            matrix.append(row)

        # Испис резултата
        print("Матрица је:")
        for row in matrix:
            for element in row:
                print(element, end=" ")
            print()

Задатак 18
----------

Напиши програм који рачуна просечну вредност свих елемената матрице димензија `m × n`.

.. activecode:: v20_zadatak18
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  
Матрица:  

1 2 3  

4 5 6  

**Излаз**:  
Просечна вредност: 3.5  

**Пример 2**:

**Улаз**:  
Матрица:  

7 8  

9 10  

**Излаз**:  
Просечна вредност: 8.5  

.. reveal:: 20_18_resenje_20_18_1
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос димензија матрице
        m = int(input("Унесите број редова (m): "))
        n = int(input("Унесите број колона (n): "))

        # Унос елемената матрице
        matrix = []
        print("Унесите елементе матрице (раздвојене размацима):")
        for i in range(m):
            row = []
            elements = input("Унесите елементе за ред", i + 1": ").split()
            for elem in elements:
                row.append(int(elem))
            matrix.append(row)

        # Израчунавање просечне вредности
        total_sum = 0
        count = 0
        for row in matrix:
            for element in row:
                total_sum += element
                count += 1

        average = total_sum / count

        # Испис резултата
        print("Просечна вредност:", average)

Задатак 19
----------

Напиши програм који проналази индекс колоне са највећим збиром елемената.

.. activecode:: v20_zadatak19
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  
Матрица:  

1 2 3  

4 5 6  

**Излаз**:  
Колона са највећим збиром: 2  

**Пример 2**:

**Улаз**:  
Матрица:  

7 8  

9 10  

**Излаз**:  
Колона са највећим збиром: 1  

.. reveal:: 20_19_resenje_20_19_1
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос димензија матрице
        m = int(input("Унесите број редова (m): "))
        n = int(input("Унесите број колона (n): "))

        # Унос елемената матрице
        matrix = []
        print("Унесите елементе матрице (раздвојене размацима):")
        for i in range(m):
            row = []
            elements = input("Унесите елементе за ред", i + 1": ").split()
            for elem in elements:
                row.append(int(elem))
            matrix.append(row)

        # Проналажење колоне са највећим збиром
        max_sum = 0
        max_index = 0
        for j in range(n):
            column_sum = 0
            for i in range(m):
                column_sum += matrix[i][j]
            if column_sum > max_sum:
                max_sum = column_sum
                max_index = j

        # Испис резултата
        print("Колона са највећим збиром:", max_index + 1)

Задатак 20
----------

Напиши програм који брише одређени ред у матрици. Корисник уноси индекс реда који треба обрисати.

.. activecode:: v20_zadatak20
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  
Матрица:  

1 2 3  

4 5 6  

7 8 9  

Индекс: 1  

**Излаз**:  

1 2 3  

7 8 9  

**Пример 2**:

**Улаз**:  
Матрица:  

10 20 30  

40 50 60  

70 80 90  

Индекс: 0  

**Излаз**:  

40 50 60  

70 80 90  

.. reveal:: 20_20_resenje_20_20_1
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос димензија матрице
        m = int(input("Унесите број редова (m): "))
        n = int(input("Унесите број колона (n): "))

        # Унос елемената матрице
        matrix = []
        print("Унесите елементе матрице (раздвојене размацима):")
        for i in range(m):
            row = []
            elements = input("Унесите елементе за ред", i + 1": ").split()
            for elem in elements:
                row.append(int(elem))
            matrix.append(row)

        # Унос индекса реда који треба обрисати
        row_to_delete = int(input("Унесите индекс реда за брисање: "))

        # Брисање изабраног реда
        if 0 <= row_to_delete < m:
            matrix.pop(row_to_delete)

        # Испис резултата
        print("Модификована матрица:")
        for row in matrix:
            for element in row:
                print(element, end=" ")
            print()
