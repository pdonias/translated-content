---
title: Array.prototype.unshift()
slug: Web/JavaScript/Reference/Global_Objects/Array/unshift
tags:
  - Array
  - JavaScript
  - Method
  - Prototype
translation_of: Web/JavaScript/Reference/Global_Objects/Array/unshift
---
{{JSRef("Global_Objects", "Array")}}

## Сводка

Метод **`unshift()`** добавляет один или более элементов в начало массива и возвращает новую длину массива.

## Синтаксис

```
arr.unshift(element1[, ...[, elementN]])
```

### Параметры

- `element1, ..., elementN`
  - : Элементы, добавляемые в начало массива.

### Возвращаемое значение

Новое свойство {{jsxref("Array.length", "length")}} объекта, над которым был вызван метод `unshift`.

## Описание

Метод `unshift` вставляет переданные значения в начало массивоподобного объекта.

Метод `unshift` не является привязанным к типу; этот метод может быть {{jsxref("Function.call", "вызван", "", 1)}} или {{jsxref("Function.apply", "применён", "", 1)}} к объектам, напоминающим массив. Объекты, не содержащие свойство `length`, отражающее последний элемент в серии последовательных числовых, начинающихся с нуля, свойств, могут повести себя неправильным образом.

## Примеры

```js
var arr = [1, 2];

arr.unshift(0); // результат вызова равен 3, новой длине массива
// arr равен [0, 1, 2]

arr.unshift(-2, -1); // = 5
// arr равен [-2, -1, 0, 1, 2]

arr.unshift([-3]);
// arr равен[[-3], -2, -1, 0, 1, 2]
```

## Спецификации

{{Specifications}}

## Совместимость с браузерами

{{Compat}}

## Смотрите также

- {{jsxref("Array.prototype.push()")}}
- {{jsxref("Array.prototype.pop()")}}
- {{jsxref("Array.prototype.shift()")}}
