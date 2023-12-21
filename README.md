## JS

### Fundamentals

- #### Variables
  - [const](#const)
  - [let](#let)
  - ~~var~~
- #### Data Types
  - ##### Primitive type
    - [number](#number)
    - [string](#string)
    - [Template literals (string) ES6](#template-literals-string-es6)
    - [boolean](#boolean)
    - [null](#null)
    - [undefined](#undefined)
    - [BigInt](#BigInt)
    - [symbol](#symbol)
  - ##### Object type
    - Special types
      - [Arrays](#arrays)
      - [Functions](#functions)
      - [Dates](#dates)
      - [Math](#math)
      - [RegExp](#regexp)
      - etc.
    - [Object](#object)

### const

Объявление const задаёт константу, то есть переменную, которую нельзя менять.

```javascript
// Присваивание значения константе
const number = 42;
```

```javascript
// Ошибка перезаписи константы
const apple = 5;
apple = 10; // ошибка
```

### let

let используется для объявления переменных, которые можно изменять после объявления.

```javascript
let age = 25; // переменная age со значением 25
```

```javascript
let age;
age = 25;
console.log(age); // Выведет: 25`,
```

### number

number — это примитивный тип данных, который представляет числовые значения.

- **number — числа в разных форматах**

```javascript
let x = 2; // целое число
let y = 3.14; // число с плавающей точкой
let z = 0xff; // шестнадцатеричное число`
```

- **Методы number**

```javascript
let num = 42.5678;

let fixedNum = num.toFixed(2); // Преобразует число в строку с двумя знаками после запятой: '42.57'
let preciseNum = num.toPrecision(4); // Представляет число с точностью до четырех знаков: '42.57'
let strNum = num.toString(); // Преобразует число в строку: '42.5678'

console.log(fixedNum); // '42.57'
console.log(preciseNum); // '42.57'
console.log(strNum); // '42.5678'
```

- **Свойства number**

```javascript
let maxNum = Number.MAX_VALUE; // Максимальное положительное число
let minNum = Number.MIN_VALUE; // Минимальное положительное число
let notANum = Number.NaN; // Значение "не числовое" (NaN)
let posInf = Number.POSITIVE_INFINITY; // Положительная бесконечность
let negInf = Number.NEGATIVE_INFINITY; // Отрицательная бесконечность

console.log(maxNum); // 1.7976931348623157e+308
console.log(minNum); // 5e-324
console.log(notANum); // NaN
console.log(posInf); // Infinity
console.log(negInf); // -Infinity
```

### string

Строка (string) в JavaScript должна быть заключена в кавычки.

- **Методы строк:**
- **Метод length**

```javascript
// Возвращает длину строки: 5
let str = "Hello";
console.log(str.length);
```

- **Метод concat**

```javascript
// Объединяет строки: "Hello World"
let str = "Hello";
console.log(str.concat(" ", "World!"));
```

- **Метод toUpperCase**

```javascript
// Преобразует строку в верхний регистр: "HELLO"
let str = "Hello";
console.log(str.toUpperCase());
```

- **Метод toLowerCase**

```javascript
// Преобразует строку в нижний регистр: "hello"
let str = "HELLO";
console.log(str.toLowerCase());
```

- **Метод indexOf**

```javascript
// Возвращает индекс первого вхождения символа 'H': 0
let str = "Hello";
console.log(str.indexOf("H"));
```

- **Метод lastIndexOf**

```javascript
// Возвращает индекс последнего вхождения символа 'l': 3
let str = "Hello";
console.log(str.lastIndexOf("l"));
```

- **Метод charAt**

```javascript
// Возвращает символ по указанному индексу: 'o'
let str = "Hello";
console.log(str.charAt(4));
```

- **Метод substring**

```javascript
// Возвращает подстроку между индексами: 'll'
let str = "Hello";
console.log(str.substring(2, 4));
```

- **Метод slice**

```javascript
// Возвращает часть строки между указанными индексами: 'el'
let str = "Hello";
console.log(str.slice(1, 3));
```

- **Метод slice**

```javascript
// Возвращает часть строки, начиная с указанной позиции с конца: 'llo'
let str = "Hello";
console.log(str.slice(-3));
```

- **Метод split**

```javascript
// Разбивает строку на массив символов: ["H", "e", "l", "l", "o"]
let str = "Hello";
console.log(str.split(""));
```

- **Метод replace**

```javascript
// Заменяет подстроку на указанную строку: "Hi"
let str = "Hello";
console.log(str.replace("ello", "i"));
```

- **Метод includes**

```javascript
// Проверяет, содержится ли указанная подстрока в строке: true
let str = "Hello";
console.log(str.includes("e"));
```

### Template literals (string) ES6

Обратные кавычки (``) позволяют создавать шаблонные строки. Они поддерживают многострочность и вставку выражений через ${}. Нестроковые значения автоматически преобразуются в строки.

- **Подстановка переменных**

```javascript
let name = "Alice";
let greeting = `Hello, ${name}!`;
console.log(greeting); // Вывод: "Hello, Alice!"
```

- **Вызов функций**

```javascript
function getAge() {
  return 25;
}
let ageStatement = `I am ${getAge()} years old.`;
console.log(ageStatement); // Вывод: "I am 25 years old."
```

- **Использование условий и тернарных операторов**

```javascript
let isAdult = true;
let adultStatus = `Is the person an adult? ${isAdult ? "Yes" : "No"}.`;
console.log(adultStatus); // Вывод: "Is the person an adult? Yes."
```

- **Использование любых JavaScript выражений**

```javascript
let a = 5, b = 10;
let sum = `The sum of ${a} and ${b} is ${a + b}.`;
console.log(sum); // Вывод: "The sum of 5 and 10 is 15."

let firstName = "John", lastName = "Doe";
let fullName = \`Full name: $\{firstName} $\{lastName.toUpperCase()}.\`;
console.log(fullName); // Вывод: "Full name: John DOE."
```

- **Многострочные строки**

```javascript
let multiLineString = `The quick
brown fox
jumps over
the lazy dog`;
console.log(multiLineString);

/* Вывод:
The quick
brown fox
jumps over
the lazy dog
*/
```

### boolean

Логический тип Boolean представляет одно из двух значений: true (истина) или false (ложь).

- **Форма записи:**

```javascript
let isTrue = true;
```

```javascript
let isFalse = false;
```

- **Выражение:**

```javascript
let x = 15;
let isBiggerThanTen = x > 10; // вернет true
```

- **Сравнить строку с числом:**

```javascript
let isFiveEqual = "5";
isFiveEqual == 5; // вернет true
```

_Если использовать оператор строгого равенства ===, то преобразования типов не произойдет, и выражение вернет значение false_

```javascript
let isFiveEqualStrict = "5";
isFiveEqualStrict === 5; // вернет false
```

- **Отрицание:**

```javascript
let isTrue = true;
let isFalse = !isTrue; // вернет false
```

```javascript
let isFalse = false;
let isTrue = !isFalse; // вернет true
```

- **О“инстинным” и “ложным” значениям в JavaScript**

```javascript
Boolean(false); // false
Boolean(undefined); // false
Boolean(null); // false
Boolean(""); // false
Boolean(NaN); // false
Boolean(0); // false
Boolean(-0); // false
Boolean(0n); // false

Boolean(true); // true
Boolean("hi"); // true
Boolean(1); // true
Boolean([]); // true
Boolean([0]); // true
Boolean([1]); // true
Boolean({}); // true
Boolean({ a: 1 }); // true
```

### null

Значение null представляет отсутствие какого-либо объектного значения.

- **Присвоение переменной значения null**

```javascript
let value = null;
console.log(value); // Выводит: null
```

- **Проверка значения на null**

```javascript
let result = null;

if (result === null) {
  console.log("Значение равно null");
} else {
  console.log("Значение не равно null");
}
```

- **Очистка значения переменной**

```javascript
let number = 10;
console.log(number); // Выводит: 10

number = null;
console.log(number); // Выводит: null
```

### undefined

undefined - это примитив, обозначающий неизвестное или отсутствующее значение. JavaScript автоматически устанавливает undefined переменным при их объявлении без присвоения значений.

- **Неинициализированная переменная**

```javascript
let variable;
console.log(variable); // Вывод: undefined
```

- **Функция без возвращаемого значения**

```javascript
function doSomething() {
  // Код функции
}

let result = doSomething();
console.log(result); // Вывод: undefined
```

- **Обращение к несуществующему свойству объекта**

```javascript
let obj = { name: "John" };
console.log(obj.age); // Вывод: undefined
```

### BigInt

BigInt – это специальный числовой тип, который предоставляет возможность работать с целыми числами произвольной длины.

- **Создать BigInt можно добавив суффикс n в конец записи числа**

```javascript
const biggy = 9997000254740991n;
```

- **Создать BigInt можно вызвав конструктор BigInt**

```javascript
const alsoBig = BigInt(9997000254999999);
```

### symbol

Символ (Symbol) — примитивный тип, значения которого создаются с помощью вызова функции Symbol. Каждый созданный символ уникален.

- **Создание**

```javascript
const sym = Symbol();
const symTwo = Symbol();

console.log(sym === symTwo);
// false
```

_Даже если описания символов совпадают, JavaScript всё равно создаёт уникальные символы_

```javascript
const sym = Symbol("name");
const symTwo = Symbol("name");

console.log(sym === symTwo);
// false
```

### Arrays

Массив — это структура, в которой можно хранить коллекции элементов — чисел, строк, других массивов и так далее. Элементы нумеруются и хранятся в том порядке, в котором их поместили в массив

- **Форма записи**

```javascript
const guestList = []; // гостей нет
```

```javascript
let fruits = ["Яблоко", "Апельсин", "Слива"];
```

- **Разные типы значений**

```javascript
let arr = [
  145,
  "Яблоко",
  { name: "Джон" },
  true,
  function () {
    alert("привет");
  },
];
```

- **Методы массивов:**
- **Метод length**

```javascript
const array = [1, 2, 3, 4];
console.log(array.length); // Вывод: 4
```

- **Метод push**

```javascript
const array = [1, 2, 3, 4];
array.push(12);
console.log(array); // Вывод: [1, 2, 3, 4, 12]
```

- **Метод unshift**

```javascript
const array = [1, 2, 3, 4];
array.unshift(12);
console.log(array); // Вывод: [12, 1, 2, 3, 4]
```

- **Метод pop**

```javascript
const array = [1, 2, 3, 4];
array.pop();
console.log(array); // Вывод: [1, 2, 3]
```

- **Метод shift**

```javascript
const array = [1, 2, 3, 4];
array.shift();
console.log(array); // Вывод: [2, 3, 4]
```

- **Метод splice**

```javascript
const array = [1, 2, 3, 4];
array.splice(0, 1);
console.log(array); // Вывод: [2, 3, 4]
```

- **Метод slice**

```javascript
const array = [1, 2, 3, 4];
console.log(array.slice(1, 2)); // Вывод: [2, 3]
```

- **Метод toString**

```javascript
const array = [1, 2, 3, 4];
console.log(array.toString()); // Вывод: "1,2,3,4"
```

- **Метод concat**

```javascript
const arr1 = [1, 2];
const arr2 = [3, 4];
console.log(arr1.concat(arr2)); // Вывод: [1, 2, 3, 4]
```

- **Метод reverse**

```javascript
const array = [1, 2, 3, 4];
console.log(array.reverse()); // Вывод: [4, 3, 2, 1]
```

- **Методы массивов (ES6):**
- **Метод map() (ES6)**

```javascript
const numbers = [1, 2, 3, 4, 5];
const doubled = numbers.map((num) => num * 2);
// Метод map: Создает новый массив, содержащий удвоенные значения исходного массива
console.log(doubled); // Результат: [2, 4, 6, 8, 10]
```

- **Метод every() (ES6)**

```javascript
const numbers = [1, 2, 3, 4, 5];
const isGreaterThanZero = numbers.every((num) => num > 0);
// Метод every: Возвращает true, если все элементы массива соответствуют указанному условию
console.log(isGreaterThanZero); // Результат: true (все элементы больше нуля)
```

- **ММетод includes() (ES6)**

```javascript
const numbers = [1, 2, 3, 4, 5];
const includesThree = numbers.includes(3);
// Метод includes: Возвращает true, если массив содержит указанный элемент
console.log(includesThree); // Результат: true (число 3 присутствует в массиве)
```

- **Итератор for...of (ES6)**

```javascript
const iterable = ["a", "b", "c"];
// Итератор for...of: Позволяет перебирать элементы итерируемых объектов, например, массивов или строк
for (const element of iterable) {
  console.log(element); // Результат: a, затем b, затем c
}
```

- **Оператор распространения Spread (ES6)**

```javascript
const arr1 = [1, 2, 3];
const arr2 = [4, 5, 6];
const merged = [...arr1, ...arr2];
// Оператор Spread: Объединяет элементы нескольких массивов в один массив
console.log(merged); // Результат: [1, 2, 3, 4, 5, 6]
```

- **Метод filter() (ES6)**

```javascript
const numbers = [1, 2, 3, 4, 5];
const evenNumbers = numbers.filter((num) => num % 2 === 0);
// Метод filter: Создает новый массив, содержащий элементы, прошедшие заданное условие
console.log(evenNumbers); // Результат: [2, 4]
```

- **Метод reduce() (ES6)**

```javascript
const numbers = [1, 2, 3, 4, 5];
const sum = numbers.reduce(
  (accumulator, currentValue) => accumulator + currentValue,
  0
);
// Метод reduce: Применяет функцию к каждому элементу массива, возвращая результирующее значение
console.log(sum); // Результат: 15 (сумма всех элементов массива)
```
