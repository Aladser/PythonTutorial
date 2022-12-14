# Кортежи

**Кортежи** - неизменяемые последовательности, содержащие произвольные данные

`empty_tuple = () # пустой кортеж`

`point = (1.5, 6.0) # кортеж из двух чисел`

`names = ('Timur', 'Ruslan', 'Roman') # кортеж из трех строк`

`info = ('Timur', 'Guev', 28, 170, 60, False) # кортеж из 6 элементов разных типов`

`nested_tuple = (('one', 'two'), ['three', 'four']) # кортеж из кортежа и списка`

Для создания кортежа с единственным элементом после значения элемента ставят замыкающую запятую:

`my_tuple = (1,)`

### Функции преобразования

Функция `list()` может применяться для преобразования кортежа в список.

Функция `tuple()`  может применяться для преобразования списка в кортеж

Функция `join()` преобразует кортеж в строку

### Кортежи поддерживают те же операции, что и списки, за исключением изменяющих содержимое.

* доступ к элементу по индексу (только для получения значений элементов);
* методы, в частности index(), count();
* встроенные функции, в частности len(), sum(), min() и max();
срезы;
* оператор принадлежности in;
* операторы конкатенации (+) и повторения (*).

### Перебор элементов

***Вариант 1*** Если нужны индексы элементов:

`numbers = (0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10)`

`for i in range(len(numbers)):`

&emsp;`print(numbers[i])`

***Вариант 2*** Если индексы не нужны:

`numbers = (0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10)`

`for num in numbers:`

&emsp;`print(num)`

### Кортежи можно сравнивать между собой.

Приведенный ниже код:

`print((1, 8) == (1, 8))`

`print((1, 8) != (1, 10))`

p`rint((1, 9) < (1, 2))`

`print((2, 5) < (6,))`

`print(('a', 'bc') > ('a', 'de'))`

выводит:

`True`

`True`

`False`

`True`

`False`

### Упаковка кортежей

`tuple1 = (1, 2, 3)`

`tuple2 = ('b',)`

`tuple3 = ('red', 'green', 'blue', 'cyan')`

### Распаковка кортежей

`colors = ('red', 'green', 'blue', 'cyan')`

`(a, b, c, d) = colors`

Как мы знаем, если при распаковке кортежа число элементов слева и справа не совпадает, то возникает ошибка времени исполнения. Есть способ собрать сразу несколько значений в одну переменную. Это делается при помощи звездочки перед именем переменной.

`a, b, *tail = 1, 2, 3, 4, 5, 6`

В этом случае в переменной a будет записана единица, в переменной b — двойка, а в переменной tail — список, состоящий из всех аргументов, которые не попали в предыдущие переменные. В данном случае tail будет равен [3, 4, 5, 6].

Распаковывать можно не только кортеж, правая сторона может быть любой последовательностью (кортеж, строка или список).
