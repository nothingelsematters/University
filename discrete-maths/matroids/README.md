# Задача A.Планирование заданий

```
Имя входного файла: schedule.in
Имя выходного файла: schedule.out
Ограничение по времени: 2 секунды
Ограничение по памяти: 256 мегабайт
```

Имеется некоторое множество заданий и один исполнитель. На выполнение одного задания уходит единица времени. Задания можно выполнять начиная с момента времени 0. У каждого задания есть две характеристики: d<sub>i</sub> и w<sub>i</sub>. Если задание не было выполнено к моменту времени d<sub>i</sub>, взимается штраф в размере w<sub>i</sub>. Требуется минимизировать суммарный штраф.

## Формат входного файла

Первая строка входного файла содержит натуральное число n — количество заданий (1 < n < 100 000). Следующие n строк содержат по два натуральных числа, разделенных пробелом — d<sub>i</sub> и w<sub>i</sub> (0 < d<sub>i</sub>, w<sub>i</sub> 10<sup>9</sup>).

## Формат выходного файла

Выведите одно число — минимальный суммарный штраф.

## Примеры

### schedule.in
```
2
1 1
1 2
```
### schedule.out
```
1
```

# Задача C. Паросочетание максимального веса

```
Имя входного файла: matching.in
Имя выходного файла: matching.out
Ограничение по времени: 2секунды
Ограничение по памяти: 256мегабайт
```

Дан двудольный граф. Количество вершин в левой и правой доле совпадает и равно n. У каждой вершины левой доли есть вес, i-й вершине соответствует вес w<sub>i</sub>. Вес просочетания, ребрам которого инцидентны вершины левой доли a<sub>1</sub>..a<sub>k</sub> есть √∑ k i = 1 w a^2 i. Требуется найти паросочетание максимального веса.

## Формат входного файла

Первая строка входного файла содержит натуральное число n — количество вершин в обеих долях (1 < n < 1000). Вторая строка входного файла содержит n целых чисел w<sub>1</sub>..w<sub>n</sub> (1 < w<sub>i</sub>  1000). Следующие n строк содержат описания ребер, инцидентных соответствующей вершине левой доли. Формат описания: количество ребер, затем номера вершин правой доли, разделенные пробелом. Суммарное количество ребер не превосходит 200000.

## Формат выходного файла

Выведите n чисел — для каждой вершины левой доли выведите номер вершины правой доли, с которой ее надо взять в паросочетание. Если вершина не входит в паросочетание, выведите 0.

## Примеры

### matching.in
```
4
1 3 2 4
4 1 2 3 4
2 1 4
2 1 4
2 1 4
```

### matching.out
```
2 1 0 4
```

# Задача D. Проверка

```
Имя входного файла: check.in
Имя выходного файла: check.out
Ограничение по времени: 2секунды
Ограничение по памяти: 256мегабайт
```

Дано некоторое семейтво множеств S < 2<sup>X</sup>. Требуется проверить, может ли S быть семейством независимых множеств некоторого матроида.

## Формат входного файла

Первая строка входного файла содержит два натуральных числа n и m — мощность множеств X и S соответственно (1 < n < 10, 0 < m < 2<sup>n</sup>). Каждая из следующих m строк содержит описание элемента множества S. Формат описания: количество элементов в подмножестве, затем через пробел номера этих элементов. Элементы множества X занумерованы начиная с единицы.

## Формат выходного файла

Выведите «`YES`» ,если S может быть семейством независимых множеств некоторого матроида и «`NO`» иначе.

## Примеры

### check.in
```
2 4
0
1 1
1 2
2 1 2
```

### check.out
YES

---

### check.in
```
2 3
0
1 1
2 1 2
```

### check.out
```
NO
```

# Задача E. Циклы
```
Имя входного файла: cycles.in
Имя выходного файла: cycles.out
Ограничение по времени: 2секунды
Ограничение по памяти: 256мегабайт
```

Дано некоторое семейство множеств S < 2<sup>X</sup>. Известно, что это множество циклов некоторого матроида. Кроме того, у каждого элемента множества X есть свой вес. Вес подможества X есть сумма весов элементов, принадлежащих ему. Требуется найти базу максимального веса.

## Формат входного файла

Первая строка входного файла содержит два натуральных числа n и m — мощность множеств X и S соответственно (1 < n < 20).

Вторая строка входного файла содержит n чисел w<sub>1</sub>..w<sub>n</sub> (1 < w<sub>i</sub> < 1000). Здесь элементы множества X занумерованы начиная с единицы и w<sub>i</sub> —вес i-го элеметам ножества X. Каждая из следующих m строк содержит описание элемента множества S.

Формат описания: количество элементов в подмножестве, затем через пробел номера этих элементов.

## Формат выходного файла

Выведите одно число — вес максимальной базы.

## Примеры

### cycles.in
```
3 1
10 20 30
3 1 3 2
```

### cycles.out
```
50
```
