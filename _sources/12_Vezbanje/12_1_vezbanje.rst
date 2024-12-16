Вежбање
========

Задатак 1
-----------

Дата је `8 × 8` шаховска табла представљена матрицом. Постоји тачно један бели топ ('R'), неколико белих ловаца ('B') и неколико црних пиона ('p'). Потребно је пронаћи колико пиона топ може да нападне.

.. activecode:: v7_zadatак5
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  
Шаховска табла:

. . . . . . . .  

. . . p . . . .  

. . . R . . . .  

. . . p . . . .  

. . . . . . . .  

. . . p . . . .  

. . . . . . . .  

. . . . . . . .  

**Излаз**:  
3  

**Пример 2**:

**Улаз**:  
Шаховска табла:

. . . . . . . .  

. . . p . . . .  

. . . B R B . .  

. . . p . . . .  

. . . . . . . .  

. . . p . . . .  

. . . . . . . .  

. . . . . . . .  

**Излаз**:  
0  

.. reveal:: 12_1_resenje_12_1_5
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос шаховске табле
        board = []
        for _ in range(8):
            row = input("Унесите ред табле (користите '.', 'R', 'B', 'p'): ").split()
            board.append(row)

        # Проналажење топа
        def find_rook(board):
            for i in range(8):
                for j in range(8):
                    if board[i][j] == 'R':
                        return i, j

        rook_x, rook_y = find_rook(board)
        count = 0

        # Провера у горњем смеру
        for i in range(rook_x - 1, -1, -1):
            if board[i][rook_y] == 'B':
                break
            if board[i][rook_y] == 'p':
                count += 1
                break

        # Провера у доњем смеру
        for i in range(rook_x + 1, 8):
            if board[i][rook_y] == 'B':
                break
            if board[i][rook_y] == 'p':
                count += 1
                break

        # Провера у левом смеру
        for j in range(rook_y - 1, -1, -1):
            if board[rook_x][j] == 'B':
                break
            if board[rook_x][j] == 'p':
                count += 1
                break

        # Провера у десном смеру
        for j in range(rook_y + 1, 8):
            if board[rook_x][j] == 'B':
                break
            if board[rook_x][j] == 'p':
                count += 1
                break

        # Испис резултата
        print(f"Бели топ напада {count} пиона.")


Задатак 2
-----------

Дате су двa стринга `str1` и `str2`. Вратите највећи подстринг `x` такав да `x` дели обе ниске.

`x` дели стринг `str` ако и само ако `str = x + x + x + ...` за неко `k > 1`.

.. activecode:: v7_zadatак6
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  
str1 = "ABABAB"  

str2 = "ABAB"  

**Излаз**:  
"AB"  

**Пример 2**:

**Улаз**:  
str1 = "PETLJA"  

str2 = "KOD"  

**Излаз**:  
""  

.. reveal:: 12_1_resenje_12_1_6
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос ниски
        str1 = input("Унесите прву ниску: ")
        str2 = input("Унесите другу ниску: ")

        # Проналажење највећег заједничког делиоца
        def gcd_of_strings(str1, str2):
            def gcd(a, b):
                while b:
                    a, b = b, a % b
                return a

            if str1 + str2 != str2 + str1:
                return ""
            length = gcd(len(str1), len(str2))
            return str1[:length]

        # Испис резултата
        print(gcd_of_strings(str1, str2))


Задатак 3
-----------

Дат је низ `flowerbed` који садржи `0` (празна парцела) и `1` (засађена парцела). 
Не могу се садити цветови на суседним парцелама. Потребно је проверити да ли је могуће засадити `n` нових цветова без кршења правила.

.. activecode:: v7_zadatак7
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  
1 0 0 0 1

n = 1  

**Излаз**:  
True  

**Пример 2**:

**Улаз**:  
1 0 0 0 1  

n = 2  

**Излаз**:  
False  

.. reveal:: 12_1_resenje_12_1_7
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос података
        flowerbed = list(map(int, input("Унесите низ flowerbed: ").split()))
        n = int(input("Унесите број n: "))

        # Провера могућности садње
        def can_place_flowers(flowerbed, n):
            count = 0
            for i in range(len(flowerbed)):
                if flowerbed[i] == 0 and (i == 0 or flowerbed[i - 1] == 0) and (i == len(flowerbed) - 1 or flowerbed[i + 1] == 0):
                    flowerbed[i] = 1
                    count += 1
                if count >= n:
                    return True
            return False

        # Испис резултата
        print(can_place_flowers(flowerbed, n))


Задатак 4
-----------

Дат је низ `s`. Потребно је обрнути све самогласнике у низу.

Самогласници су `a`, `e`, `i`, `o`, `u` и могу се јавити и као мала и као велика слова.

.. activecode:: v7_zadatак8
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  
"hello"  

**Излаз**:  
"holle"  

**Пример 2**:

**Улаз**:  
"petlja"  

**Излаз**:  
"patlje"  

.. reveal:: 12_1_resenje_12_1_8
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос низа
        s = input("Унесите низ: ")

        # Обртање самогласника
        def reverse_vowels(s):
            vowels = "aeiouAEIOU"
            s = list(s)
            i, j = 0, len(s) - 1
            while i < j:
                if s[i] in vowels and s[j] in vowels:
                    s[i], s[j] = s[j], s[i]
                    i += 1
                    j -= 1
                if s[i] not in vowels:
                    i += 1
                if s[j] not in vowels:
                    j -= 1
            return "".join(s)

        # Испис резултата
        print(reverse_vowels(s))


Задатак 5
-----------

Дат је `3 x 3` филтер који се примењује на сваку ћелију матрице. 
Филтер израчунава просек вредности ћелије и њених суседних ћелија. Ако нека од суседних ћелија недостаје, она се не узима у обзир.

.. activecode:: v7_zadatак9
    :coach:

    # Допуни

**Пример 1**:

**Улаз**:  
Матрица:

1 1 1  

1 0 1  

1 1 1  

**Излаз**:  
Нова матрица:

0 0 0  

0 0 0  

0 0 0  

**Пример 2**:

**Улаз**:
Матрица:

1 2 3

4 5 6

7 8 9

**Излаз**:
Нова матрица:

2 3 3

5 6 6

8 9 9

.. reveal:: 12_1_resenje_12_1_9
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code-block:: python

        # Унос матрице
        m, n = map(int, input("Унесите димензије матрице (m n): ").split())
        matrix = []
        for _ in range(m):
            row = list(map(int, input("Унесите ред матрице: ").split()))
            matrix.append(row)

        # Примена филтера
        def image_smoother(matrix):
            m, n = len(matrix), len(matrix[0])
            result = [[0] * n for _ in range(m)]
            directions = [(-1, -1), (-1, 0), (-1, 1), (0, -1), (0, 0), (0, 1), (1, -1), (1, 0), (1, 1)]

            for i in range(m):
                for j in range(n):
                    total, count = 0, 0
                    for di, dj in directions:
                        ni, nj = i + di, j + dj
                        if 0 <= ni < m and 0 <= nj < n:
                            total += matrix[ni][nj]
                            count += 1
                    result[i][j] = total // count
            return result

        # Испис резултата
        smoothed_matrix = image_smoother(matrix)
        for row in smoothed_matrix:
            print(" ".join(map(str, row)))
