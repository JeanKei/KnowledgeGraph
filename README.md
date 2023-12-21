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
    - [Template literals (string) ES6](<#Template-literals-(string)-ES6>)
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
