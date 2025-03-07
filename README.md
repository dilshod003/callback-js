# callback-js

## Функция обратного вызова — это функция, передаваемая в другую функцию в качестве аргумента, которая затем вызывается внутри внешней функции для завершения какой-либо процедуры или действия. Потребитель API на основе обратного вызова пишет функцию, которая передается в API. Поставщик API (называемый вызывающей стороной ) берет функцию и вызывает ее обратно (или выполняет) в какой-то момент внутри тела вызывающей стороны. Вызывающая сторона отвечает за передачу правильных параметров в функцию обратного вызова. Вызывающая сторона также может ожидать определенного возвращаемого значения от функции обратного вызова, которое используется для указания дальнейшего поведения вызывающей стороны.

### Массив.прототип.reduce()
##### Метод reduce()экземпляров Arrayвыполняет пользовательскую функцию обратного вызова "редуктора" для каждого элемента массива по порядку, передавая возвращаемое значение из вычисления для предыдущего элемента. Конечный результат запуска редуктора по всем элементам массива — одно значение. При первом запуске обратного вызова нет «возвращаемого значения предыдущего вычисления». Если указано, вместо него может использоваться начальное значение. В противном случае элемент массива с индексом 0 используется в качестве начального значения, и итерация начинается со следующего элемента (индекс 1 вместо индекса 0).

```
const array1 = [1, 2, 3, 4];

// 0 + 1 + 2 + 3 + 4
const initialValue = 0;
const sumWithInitial = array1.reduce(
  (accumulator, currentValue) => accumulator + currentValue,
  initialValue,
);

console.log(sumWithInitial);
// Expected output: 10

```

###### Функция для выполнения для каждого элемента массива. Ее возвращаемое значение становится значением accumulatorпараметра при следующем вызове callbackFn. Для последнего вызова возвращаемое значение становится возвращаемым значением reduce(). Функция вызывается со следующими аргументами:

### accumulator
#### Значение, полученное в результате предыдущего вызова callbackFn. При первом вызове его значение равно , initialValueесли последний указан; в противном случае его значение равно array[0].
### currentValue
#### Значение текущего элемента. При первом вызове его значение равно , array[0]если initialValueуказано ; в противном случае его значение равно array[1].
### currentIndex
#### Позиция индекса currentValueв массиве. При первом вызове его значение равно , 0если initialValueуказано , в противном случае 1.

## Массив.прототип.map()
#### Метод map()экземпляров Arrayсоздает новый массив, заполненный результатами вызова предоставленной функции для каждого элемента в вызывающем массиве.
```
const array1 = [1, 4, 9, 16];

// Pass a function to map
const map1 = array1.map((x) => x * 2);

console.log(map1);
// Expected output: Array [2, 8, 18, 32]
```

### Метод map()является итеративным методом . Он вызывает предоставленную callbackFnфункцию один раз для каждого элемента массива и создает новый массив из результатов. Прочтите раздел итеративных методов для получения дополнительной информации о том, как эти методы работают в целом.


## Массив.прототип.toSorted()
### Метод toSorted()instances Array— это копирующая версия метода sort(). Он возвращает новый массив с элементами, отсортированными по возрастанию.

```
const months = ["Mar", "Jan", "Feb", "Dec"];
const sortedMonths = months.toSorted();
console.log(sortedMonths); // ['Dec', 'Feb', 'Jan', 'Mar']
console.log(months); // ['Mar', 'Jan', 'Feb', 'Dec']

const values = [1, 10, 21, 2];
const sortedValues = values.toSorted((a, b) => a - b);
console.log(sortedValues); // [1, 2, 10, 21]
console.log(values); // [1, 10, 21, 2]
```

## Массив.прототип.find()
### Метод find()экземпляров Arrayвозвращает первый элемент в предоставленном массиве, который удовлетворяет предоставленной функции тестирования. Если ни одно значение не удовлетворяет функции тестирования, undefinedвозвращается.
```
const array1 = [5, 12, 8, 130, 44];

const found = array1.find((element) => element > 10);

console.log(found);
// Expected output: 12

```

