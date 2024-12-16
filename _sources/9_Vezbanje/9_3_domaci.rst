Домаћи задаци
=============

Уз сваки задатак добијате кôд који треба да решава дати проблем. Кôд који добијате није исправан. Ваш задатак је да откријете зашто и исправите кôд.

Задатак 1
---------

Креирати функцију која додаје дати елемент на крај листе.

.. activecode:: 9_3_domaci_1
    :coach:

    def dodaj_element(lista, element):
        lista = lista + [element]


Задатак 2
---------

Креирати функцију која дати број инкрементира за 5.

.. activecode:: 9_3_domaci_2
    :coach:

    def inkrementiraj_za_5(broj):
        broj += 5


Задатак 3
---------

Креирати функцију која за дату листу враћа листу у којој је сваки елемент листе једнак квадрату тог елемента сабрано са тим елементом.

.. activecode:: 9_3_domaci_3
    :coach:

    def kvadrat_plus_element(lista):    
        kvadrat_lista = lista

        for i in range(len(kvadrat_lista)):
            kvadrat_lista[i] = kvadrat_lista[i] ** 2 
            kvadrat_lista[i] += lista[i]
        
        return kvadrat_lista

Задатак 4
---------

Креирај функцију која враћа обрнуту листу.

.. activecode:: 9_3_domaci_4
    :coach:

    def obrni_listu(lista):
        nova_lista = lista
        return nova_lista.reverse()

    