## JS

### Fundamentals

- Variables
  - [const](#const)
  - [let](#let)
  - ~~var~~
- Data Types
  - Primitive type
    - [number](#number)
    - [string](#string)
    - [Template literals (string) ES6](#template-literals-string-es6)
    - [boolean](#boolean)
    - [null](#null)
    - [undefined](#undefined)
    - [symbol](#symbol)
    - [bigint](#bigint)

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

- **Методы строк**

```javascript
// Возвращает длину строки: 5
let str = "Hello";
console.log(str.length);
```

```javascript
// Объединяет строки: "Hello World"
let str = "Hello";
console.log(str.concat(" ", "World!"));
```

```javascript
// Преобразует строку в верхний регистр: "HELLO"
let str = "Hello";
console.log(str.toUpperCase());
```

```javascript
// Преобразует строку в нижний регистр: "hello"
let str = "HELLO";
console.log(str.toLowerCase());
```

```javascript
// Возвращает индекс первого вхождения символа 'H': 0
let str = "Hello";
console.log(str.indexOf("H"));
```

```javascript
// Возвращает индекс последнего вхождения символа 'l': 3
let str = "Hello";
console.log(str.lastIndexOf("l"));
```

```javascript
// Возвращает символ по указанному индексу: 'o'
let str = "Hello";
console.log(str.charAt(4));
```

```javascript
// Возвращает подстроку между индексами: 'll'
let str = "Hello";
console.log(str.substring(2, 4));
```

```javascript
// Возвращает часть строки между указанными индексами: 'el'
let str = "Hello";
console.log(str.slice(1, 3));
```

```javascript
// Возвращает часть строки, начиная с указанной позиции с конца: 'llo'
let str = "Hello";
console.log(str.slice(-3));
```

```javascript
// Разбивает строку на массив символов: ["H", "e", "l", "l", "o"]
let str = "Hello";
console.log(str.split(""));
```

```javascript
// Заменяет подстроку на указанную строку: "Hi"
let str = "Hello";
console.log(str.replace("ello", "i"));
```

```javascript
// Проверяет, содержится ли указанная подстрока в строке: true
let str = "Hello";
console.log(str.includes("e"));
```

### Template literals (string) ES6

Шаблонные строки — это ещё один способ создания строк, наравне с одинарными или двойными кавычками. Шаблонные строки объявляются с помощью обратных кавычек. Шаблонная строка может быть многострочной, все переносы строк в ней будут сохранены. В шаблонной строке с помощью синтаксиса ${ } можно использовать любые выражения JavaScript. Любой нестроковый результат (например, объект) будет приведён к строке. Шаблонные строки сейчас — основной способ работы со строками, в которые нужно подставлять вычисляемые значения.

- **Подстановка переменных:**

```javascript
let name = "Alice";
let greeting = `Hello, ${name}!`;
console.log(greeting); // Вывод: "Hello, Alice!"
```

- **Вызов функций:**

```javascript
function getAge() {
  return 25;
}
let ageStatement = `I am ${getAge()} years old.`;
console.log(ageStatement); // Вывод: "I am 25 years old."
```

- **Использование условий и тернарных операторов:**

```javascript
let isAdult = true;
let adultStatus = `Is the person an adult? ${isAdult ? "Yes" : "No"}.`;
console.log(adultStatus); // Вывод: "Is the person an adult? Yes."
```

- **Использование любых JavaScript выражений:**

```javascript
let a = 5, b = 10;
let sum = `The sum of ${a} and ${b} is ${a + b}.`;
console.log(sum); // Вывод: "The sum of 5 and 10 is 15."

let firstName = "John", lastName = "Doe";
let fullName = \`Full name: $\{firstName} $\{lastName.toUpperCase()}.\`;
console.log(fullName); // Вывод: "Full name: John DOE."
```

- **Многострочные строки:**

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
