# Paradigms of Programming
## [Домашнее задание 1. Хэширование](1-calc-sha256)

Модификации
 * *Сложная*
    * Класс должен иметь имя `CalcSHA256` и подсчитывать [SHA-256](https://en.wikipedia.org/wiki/Secure_Hash_Algorithm)
 * *Простая*
    * Напишите простой аналог утилиты [sha256sum](http://linux.die.net/man/1/sha256sum)
    * Класс должен называться `SHA256Sum`
    * Список файлов для хэширования передается в виде аргументов командной строки
    * Если список файлов пуст, то хэшируется стандартный ввод а именем файла считается `-`
    * Вывод хэшей осуществляется в формате `<хэш> *<имя файла>`

## [Домашнее задание 2. Бинарный поиск](2-binary-search)

Модификации
 * *Базовая*
    * Класс `BinarySearch` должен находиться в пакете `search`
 * *Простая*
    * Если в массиве `a` отсутствует элемент, равный `x`, то требуется
      вывести индекс вставки в формате, определенном в
      [`Arrays.binarySearch`](http://docs.oracle.com/javase/8/docs/api/java/util/Arrays.html#binarySearch-int:A-int-).
    * Класс должен иметь имя `BinarySearchMissing`
 * *Сложная*
    * Требуется вывести два числа: начало и длину диапазона элементов,
      равных `x`. Если таких элементов нет, то следует вывести
      пустой диапазон, у которого левая граница совпадает с местом
      вставки элемента `x`.
    * Не допускается использование типов `long` и `BigInteger`.
    * Класс должен иметь имя `BinarySearchSpan`

## [Домашнее задание 3. Очередь на массиве](3-array-queue)

Модификации
 * *Базовая*
    * Классы должны находиться в пакете `queue`
 * *Простая*
    * Реализовать метод `toArray`, возвращающий массив,
      содержащий элементы, лежащие в очереди в порядке
      от головы к хвосту.
    * Исходная очередь должна остаться неизменной
    * Дублирования кода быть не должно
 * *Сложная*
    * Реализовать методы
        * `push` – добавить элемент в начало очереди
        * `peek` – вернуть последний элемент в очереди
        * `remove` – вернуть и удалить последний элемент из очереди

## [Домашнее задание 4. Очередь на связном списке](4-queue)

Модификации
 * *Простая*
    * Добавить в интерфейс очереди и реализовать метод
      `toArray`, возвращающий массив,
      содержащий элементы, лежащие в очереди в порядке
      от головы к хвосту
    * Исходная очередь должна оставаться неизменной
    * Дублирования кода быть не должно
 * *Сложная*
    * Добавить в интерфейс очереди и реализовать методы
        * `filter(predicate)` – создать очередь, содержащую элементы, удовлетворяющие
            [предикату](https://docs.oracle.com/javase/8/docs/api/java/util/function/Predicate.html)
        * `map(function)` – создать очередь, содержащую результаты применения
            [функции](https://docs.oracle.com/javase/8/docs/api/java/util/function/Function.html)
    * Исходная очередь должна остаться неизменной
    * Тип возвращаемой очереди должен соответствовать типу исходной очереди
    * Взаимный порядок элементов должен сохраняться
    * Дублирования кода быть не должно

## [Домашнее задание 5. Вычисление выражений](5-evaluate)

Модификации
 * *Базовая*
    * Реализовать интерфейс `Expression`
 * *Простая*
    * Реализовать интерфейс `DoubleExpression`
 * *Сложная*
    * Реализовать интерфейсы `DoubleExpression` и `TripleExpression`

## [Домашнее задание 6. Разбор выражений](6-expression-parser)

Модификации
 * *Базовая*
    * Класс `ExpressionParser` должен реализовывать интерфейс
        `Parser`
    * Результат разбора должен реализовывать интерфейс
        `TripleExpression`
 * *Простая*
    * Дополнительно реализовать бинарные операции:
        * `&` — побитное И, приоритет меньше чем у `+` (`6 & 1 + 2` равно `6 & (1 + 2)` равно 2);
        * `^` — побитный XOR, приоритет меньше чем у `&` (`6 ^ 1 + 2` равно `6 ^ (1 + 2)` равно 5);
        * `|` — побитное ИЛИ, приоритет меньше чем у `^` (`6 | 1 + 2` равно `6 | (1 + 2)` равно 7);
 * *Сложная*
    * Реализовать операции из простой модификации.
    * Дополнительно реализовать унарные операции (приоритет как у унарного минуса):
        * `~` — побитное отрицание, `~-5` равно 4;
        * `count` — число установленных битов, `count -5` равно 31.

## [Домашнее задание 7. Обработка ошибок](7-exceptions)

Модификации
 * *Базовая*
    * Класс `ExpressionParser` должен реализовывать интерфейс `Parser`
    * Классы `CheckedAdd`, `CheckedSubtract`, `CheckedMultiply`,
        `CheckedDivide` и `CheckedNegate` должны реализовывать интерфейс `TripleExpression`
    * Нельзя использовать типы `long` и `double`
    * Нельзя использовать методы классов `Math` и `StrictMath`
 * *Простая*
    * Дополнительно реализовать унарные операции:
        * `log10` — логарифм по уснованию 10, `log10 1000` равно 3;
        * `pow10` — 10 в степени, `pow10 4` равно 10000.
 * *Сложная*
    * Реализовать операции простой модификации.
    * Дополнительно реализовать бинарные операции (максимальный приоритет):
        * `**` — возведение в степень, `2 ** 3` равно 8;
        * `//` — логарифм, `10 // 2` равно 3.

## Домашнее задание 8. Вычисление в различных типах

Модификации
 * *Базовая*
    * Класс `GenericTabulator` должен реализовывать интерфейс `Tabulator` и
      сроить трехмерную таблицу значений заданного выражения.
        * `mode` — режим вычислений:
           * `i` — вычисления в `int` с проверкой на переполнение;
           * `d` — вычисления в `double` без проверки на переполнение;
           * `bi` — вычисления в `BigInteger`.
        * `expression` — выражение, для которого надо построить таблицу;
        * `x1`, `x2` — минимальное и максимальное значения переменной `x` (включительно)
        * `y1`, `y2`, `z1`, `z2` — аналогично для `y` и `z`.
        * Результат: элемент `result[i][j][k]` должен содержать
          значение выражения для `x = x1 + i`, `y = y1 + j`, `z = z1 + k`.
          Если значение не определено (например, по причине переполнения),
          то соответствующий элемент должен быть равен `null`.
 * *Простая*
    * Дополнительно реализовать поддержку режимов:
        * `u` — вычисления в `int` без проверки на переполнение;
        * `l` — вычисления в `long` без проверки на переполнение;
        * `s` — вычисления в `s` без проверки на переполнение.
 * *Сложная*
    * Реализовать операции из простой модификации.
    * Дополнительно реализовать унарные операции:
        * `count` — число установленных битов, `count 5` равно 2.
    * Дополнительно реализовать бинарную операцию (минимальный приоритет):
        * `min` — минимум, `2 min 3` равно 2;
        * `max` — максимум, `2 max 3` равно 3.
    * Дополнительно реализовать поддержку режимов:
        * `u` — вычисления в `int` без проверки на переполнение;
        * `l` — вычисления в `long` без проверки на переполнение;
        * `s` — вычисления в `s` без проверки на переполнение.

## [Домашнее задание 9. Функциональные выражения на JavaScript](9-functional-expression)

Модификации
 * *Базовая*
    * Код должен находиться в файле `functionalExpression.js`.
 * *Простая*. Дополнительное реализовать поддержку:
    * переменных: `y`, `z`;
    * унарных функций:
        * `negate` — смена знака, `-2 negate` равно 2;
        * `cube` — возведение в куб, `2 cube` равно 8;
        * `cuberoot` — кубический корень, `8 cuberoot` равно 2;
 * *Сложная*. Дополнительное реализовать поддержку:
    * переменных: `y`, `z`;
    * констант:
        * `pi` — π;
        * `e` — основание натурального логарифма;
    * операций:
        * `negate` — смена знака, `-2 negate` равно 2;
        * `min3` — минимальный из трех элементов, `3 1 4 min3` равно 1;
        * `max5` — максимальный из пяти элементов, `3 1 4 0 2 max5` равно 4.

## [Домашнее задание 10. Объектные выражения на JavaScript](10-object-expression)

Модификации
 * *Базовая*
    * Код должен находиться в файле `objectExpression.js`.
 * *Модификация*. Дополнительное реализовать поддержку:
    * унарных операций:
        * `Square` (`square`) — возведение в квадрат, `3 square` равно 9;
        * `Sqrt` (`sqrt`) — извлечение квадратного корня из модуля аргумента, `-9 sqrt` равно 3;
 * *Модификация*. Дополнительное реализовать поддержку:
    * бинарных операций:
        * `Power` (`pow`) — возведение в степень, `2 3 pow` равно 8;
        * `Log` (`log`) — логарифм абсолютного значения аргумента
            по абсолютному значению основания `-2 -8 log` равно 3;

## Домашнее задание 11. Обработка ошибок на JavaScript

Модификации
 * *Базовая*
    * Код должен находиться в файле `objectExpression.js`.
 * *Простая*. Дополнительное реализовать поддержку:
    * унарных операций:
        * `ArcTan` (`atan`) — арктангенс, `(atan 2)` примерно равно 1.1;
        * `Exp` (`Exp`) — экспонента, `(exp 3)` примерно равно 20;
 * *Сложная*. Дополнительное реализовать поддержку выражений в постфиксной записи:
    * `(2 3 +)` равно 5

## Домашнее задание 12. Линейная алгебра на Clojure

Модификации
 * *Базовая*
    * Код должен находиться в файле `linear.clj`.
 * *Простая*
    * Добавьте операции поэлементного сложения (`s+`),
        вычитания (`s-`) и умножения (`s*`) чисел и
        векторов любой (в том числе, переменной) формы.
        Например, `(s+ [[1 2] 3] [[4 5] 6])` должно быть равно `[[5 7] 9]`.
 * *Сложная*
    * Назовем _тензором_ многомерную прямоугольную таблицу чисел.
    * _Форма_ тензора – последовательность чисел
        (_s_<sub>1..n</sub>)=(_s_<sub>1</sub>, _s_<sub>2</sub>, …, _s<sub>n</sub>_), где
        _n_ – размерность тензора, а _s<sub>i</sub>_ – число элементов
        по _i_-ой оси.
      Например, форма тензора `[ [ [2 3 4] [5 6 7] ] ]`  равна (1, 2, 3),
      а форма `1` равна ().
    * Тензор формы (_s_<sub>1.._n_</sub>) может быть _распространен_ (broadcast)
      до тензора формы (_u_<sub>1.._m_</sub>), если (_s_<sub>i.._n_</sub>) является
      суффиксом (_u<sub>1..m</sub>_). Для этого, исходный тензор копируется
      по недостающим осям.
      Например, распространив тензор `[ [2] [3] ]` формы (2, 1) до
      формы (3, 2, 1) получим `[ [ [2] [3] ] [ [2] [3] ] [ [2] [3] ] ]`,
      а распространив `1` до формы (2, 3) получим `[ [1 1 1] [1 1 1] ]`.
    * Тензоры называются совместимыми, если один из них может быть распространен
      до формы другого.
      Например, тензоры формы (3, 2, 1) и (2, 1) совместимы, а
      (3, 2, 1) и (1, 2) – нет. Числа совместимы с тензорами любой формы.
    * Добавьте операции поэлементного сложения (`b+`),
      вычитания (`b-`) и умножения (`b*`) совместимых тензоров.
      Если формы тензоров не совпадают, то тензоры меньшей размерности
      должны быть предварительно распространены до тензоров большей размерности.
      Например, `(b+ 1 [ [10 20 30] [40 50 60] ] [100 200 300] )` должно
      быть равно `[ [111 221 331] [141 251 361] ]`.

## Домашнее задание 13. Функциональные выражения на Clojure

Модификации
 * *Базовая*
    * Код должен находиться в файле `expression.clj`.
 * *Модификация*. Дополнительное реализовать поддержку:
    * унарных операций:
        * `Sinh` (`sinh`) — гиперболический синус, `(sinh 3)` немного больше 10;
        * `Cosh` (`cosh`) — гиперболический косинус, `(cosh 3)` немного меньше 10.
