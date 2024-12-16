
Домаћи задаци
::::::::::::::

Задатак 1
`````````

**Текст задатка:**  

Направите функцију која рачуна збир цифара датог броја.

.. activecode:: 9_1_zadatak_1
    :coach:

    def zbir_cifara(broj):
        zbir = 0

        # Dopuni
        
        return zbir

    n = int(input())
    print("Zbir cifara broja", n, "je", zbir_cifara(n))

**Пример 1**:

**Улаз**:  
1234  

**Излаз**:  
Zbir cifara broja 1234 je 10

**Пример 2**:

**Улаз**:  
-567  

**Излаз**:  
Zbir cifara broja -567 je 18

.. reveal:: 9_1_resenje_1
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code::

        def zbir_cifara(broj):
            broj = abs(broj)
            zbir = 0
            while broj > 0:
                zbir += broj % 10
                broj //= 10
            return zbir


Задатак 2
`````````

**Текст задатка:**  

Нaпишите функцију која проверава да ли је број прост.

.. activecode:: 9_1_zadatak_2
    :coach:

    def je_prost(broj):
        if broj < 2:
            return # Dopuni
        for i in range(2, broj):
            if broj % i == 0:
                # Dopuni
        # Dopuni

    n = int(input())
    if je_prost(n):
        print("Broj", n, "je prost.")
    else:
        print("Broj", n, "nije prost.")

**Пример 1**:

**Улаз**:  
11  

**Излаз**:  
Broj 11 je prost. 

**Пример 2**:

**Улаз**:  
12  

**Излаз**:  
Broj 12 nije prost.

.. reveal:: 9_1_resenje_2
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code::

        def je_prost(broj):
            if broj < 2:
                return False
            for i in range(2, broj):
                if broj % i == 0:
                    return False
            return True


Задатак 3
`````````

**Текст задатка:**  

Нaпишите функцију која рачуна факторијал броја (рекурзивно решење).

.. activecode:: 9_1_zadatak_3
    :coach:

    def faktorijal(n):
        # Baza
        if # Dopuni
            return # Dopuni
        # Rekurzija
        return # Dopuni
    
    n = int(input())
    print(faktorijal(n))

**Пример 1**:

**Улаз**:  
5  

**Излаз**:  
120  

**Пример 2**:

**Улаз**:  
3  

**Излаз**:  
6  

.. reveal:: 9_1_resenje_3
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code::

        def faktorijal(n):
            if n == 0 or n == 1:
                return 1
            return n * faktorijal(n - 1)


Задатак 4
`````````

**Текст задатка:**  

Напишите функцију која генерише првих `n` бројева Фибоначијевог низа.

.. activecode:: 9_1_zadatak_4
    :coach:

    def fibonacci(n):
        niz = []
        
        # Dopuni

        return niz

    n = int(input())
    for broj in fibonacci(n):
        print(broj, end=" ")

**Пример 1**:

**Улаз**:  
5  

**Излаз**:  
0 1 1 2 3

**Пример 2**:

**Улаз**:  
8  

**Излаз**:  
0 1 1 2 3 5 8 13

.. reveal:: 9_1_resenje_4
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code::

        def fibonacci(n):
            niz = []
            a, b = 0, 1
            for _ in range(n):
                niz.append(a)
                a, b = b, a + b
            return niz

Задатак 5
`````````

**Текст задатка:**  

Направите функцију која инвертује стринг, а затим функцију која проверава да ли је стринг палиндром.

.. activecode:: 9_1_zadatak_5
    :coach:

    def inverzija(string):
        # Dopuni

    def je_palindrom(string):
        # Dopuni

    s = input()
    if je_palindrom(s):
        print("True")
    else:
        print("False")

**Пример 1**:

**Улаз**:  
radar  

**Излаз**:  
True  

**Пример 2**:

**Улаз**:  
hello  

**Излаз**:  
False  

.. reveal:: 9_1_resenje_5
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code::

        def inverzija(string):
            rezultat = ""
            for slovo in string:
                rezultat = slovo + rezultat
            return rezultat

        def je_palindrom(string):
            obrnuti = inverzija(string)
            return string == obrnuti


Задатак 6
`````````

**Текст задатка:**  

Направите функцију која враћа листу свих делилаца датог броја.

.. activecode:: 9_1_zadatak_6
    :coach:

    def delioci_broja(n):
        delioci = []
        
        # Dopuni

        return delioci

    n = int(input())
    for broj in delioci_broja(n):
        print(broj, end=" ")

**Пример 1**:

**Улаз**:  
12  

**Излаз**:  
1 2 3 4 6 12

**Пример 2**:

**Улаз**:  
15  

**Излаз**:  
1 3 5 15

.. reveal:: 9_1_resenje_6
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code::

        def delioci_broja(n):
            delioci = []
            for i in range(1, n + 1):
                if n % i == 0:
                    delioci.append(i)
            return delioci


Задатак 7
`````````

**Текст задатка:**  

Напишите функцију која ротира листу удесно за `k` позиција.

.. activecode:: 9_1_zadatak_8
    :coach:

    def rotiraj_lista(lista, k):
        # Dopuni

    niz = int(input().split())
    k = int(input())
    nova_lista = rotiraj_lista(niz, k)
    for broj in nova_lista:
        print(broj, end=" ")

**Пример 1**:

**Улаз**:  
10 20 30 40
2

**Излаз**:  
30 40 10 20

**Пример 2**:

**Улаз**:  
10 20 30 40
1

**Излаз**:  
40 10 20 30


.. reveal:: 9_1_resenje_8
    :showtitle: Прикажи решење
    :hidetitle: Сакриј решење

    .. code::

        def rotiraj_lista(lista, k):
            n = len(lista)
            k = k % n
            nova_lista = lista[-k:] + lista[:-k]
            return nova_lista
