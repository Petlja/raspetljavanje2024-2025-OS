Вежбање
========

Задатак 1
-----------

Дата је дводимензионална матрица бројева `nums`. Потребно је пронаћи највећи прост број који се налази на бар једној од дијагонала матрице. 
Ако ни један прост број није присутан, исписати 0.

.. activecode:: v12_zadatak1
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  
Матрица:  

2 3 5  

7 11 13  

17 19 23  

**Излаз**:  
23  

**Објашњење излаза**:  
Највећи прост број на дијагоналама је 23.  

**Пример 2**:

**Улаз**:  
Матрица:  

4 6 8  

10 12 14  

16 18 20  

**Излаз**:  
0  

**Објашњење излаза**:  
На дијагоналама не постоји прост број.  

.. reveal:: 12_1_resenje_12_1_1
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        def is_prime(num):
            if num < 2:
                return False
            for i in range(2, int(num ** 0.5) + 1):
                if num % i == 0:
                    return False
            return True

        def largest_prime_on_diagonals(matrix):
            largest_prime = 0
            for i in range(len(matrix)):
                if is_prime(matrix[i][i]):
                    largest_prime = max(largest_prime, matrix[i][i])
                if is_prime(matrix[i][len(matrix) - i - 1]):
                    largest_prime = max(largest_prime, matrix[i][len(matrix) - i - 1])
            return largest_prime
        
        # Ova funkcija će se koristiti u ostalim rešenjima bez definisanja
        # Pretpostavlja se da je funkcija već definisana
        def input_matrix(m, n):
            # Inicijalizacija prazne matrice
            matrica = []

            # Unos elemenata matrice
            print("Unesite elemente matrice red po red (razdvojene razmakom):")
            for i in range(m):
                red = []
                print(f"Red {i + 1}:")
                elementi = input().split()
                for elem in elementi:
                    red.append(int(elem))
                matrica.append(red)

                return matrica

        # Unos dimenzija matrice
        m = int(input("Unesite broj redova (m): "))
        n = int(input("Unesite broj kolona (n): "))
        
        # Unos matrice
        matrica = input_matrix(m, n)

        print(largest_prime_on_diagonals(matrica))  # Испис резултата


Задатак 2
-----------

Дата је матрица димензија `m × n` и број `k`. Потребно је померити матрицу удесно `k` пута.

.. activecode:: v12_zadatak2
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  
Матрица:  

1 2 3  

4 5 6  

Број k: 2  

**Излаз**:  
Матрица након померања:  

2 3 1  

5 6 4  

**Пример 2**:

**Улаз**:  
Матрица:  

7 8 9  

10 11 12  

Број k: 1  

**Излаз**:  
Матрица након померања:  

9 7 8  

12 10 11  

.. reveal:: 12_1_resenje_12_1_2
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        def shift_matrix_right(matrix, k):
            rows, cols = len(matrix), len(matrix[0])
            k = k % cols  # Уклонити вишак померања
            for i in range(rows):
                row = matrix[i]
                matrix[i] = row[-k:] + row[:-k]
            return matrix

        # Unos dimenzija matrice
        m = int(input("Unesite broj redova (m): "))
        n = int(input("Unesite broj kolona (n): "))
        
        # Unos matrice
        matrix = input_matrix(m, n)

        k = 2
        result = shift_matrix_right(matrix, k)
        for row in result:
            print(*row)  # Испис резултата


Задатак 3
-----------

Дате су две бинарне матрице `mat` и `target` димензија `n × n`. 
Проверите да ли је могуће добити `target` од `mat` ротацијом `mat` у инкрементима од 90 степени.

.. activecode:: v12_zadatak3
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  
Матрица `mat`:  

1 0  

0 1  

Матрица `target`:  

0 1  

1 0  

**Излаз**:  
True  

**Пример 2**:

**Улаз**:  
Матрица `mat`:  

1 1  

0 0  

Матрица `target`:  

1 0  

1 0  

**Излаз**:  
False  

.. reveal:: 12_1_resenje_12_1_3
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        def rotate_matrix(mat):
            n = len(mat)
            rotated = [[0] * n for _ in range(n)]
            for i in range(n):
                for j in range(n):
                    rotated[j][n - i - 1] = mat[i][j]
            return rotated

        def can_match_target(mat, target):
            for _ in range(4):  # До 4 ротације
                if mat == target:
                    return True
                mat = rotate_matrix(mat)
            return False

        # Unos dimenzija matrice
        n = int(input("Unesite broj kolona (n): "))
        
        # Unos matrice
        mat = input_matrix(n, n)
        target = input_matrix(n, n)

        print(can_match_target(mat, target))  # Испис резултата


Задатак 4
-----------

Дат је улазни низ `s`. Потребно је обрнути редослед речи у низу.

.. activecode:: v7_zadatak4
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  
"Python је забаван"

**Излаз**:  
"забаван је Python"

**Пример 2**:

**Улаз**:  
"Пример    са  размацима"

**Излаз**:  
"размацима са Пример"

.. reveal:: 12_1_resenje_12_1_4
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос низа
        s = input("Унесите низ: ")

        # Обртање редоследа речи
        words = s.split()
        reversed_words = " ".join(words[::-1])

        # Испис резултата
        print(reversed_words)
