---
title: String.raw()
slug: Web/JavaScript/Reference/Global_Objects/String/raw
tags:
  - ECMAScript6
  - Experimental
  - Expérimental(2)
  - JavaScript
  - Method
  - Reference
  - Référence(2)
  - String
translation_of: Web/JavaScript/Reference/Global_Objects/String/raw
---
{{JSRef("Global_Objects", "String")}}

## Сводка

Статический метод **`String.raw()`** является теговой функцией для [шаблонных строк](/ru/docs/Web/JavaScript/Reference/template_strings); подобно префиксу `r` в Python или префиксу `@` в C# для строковых литералов, эта функция используется для получения необработанной строки из шаблона.

## Синтаксис

```

String.raw(callSite, ...substitutions)

String.raw`templateString`
```

### Параметры

- `callSite`
  - : Правильно сформированный объект вызова, например `{ raw: 'string' }`.
- `...substitutions`
  - : Значения подстановок.
- `templateString`
  - : [Шаблонная строка](/ru/docs/Web/JavaScript/Reference/template_strings), возможно с подстановками (`${...}`).

### Выбрасываемые исключения

- {{jsxref("Global_Objects/TypeError", "TypeError")}}
  - : Если первый аргумент не является правильно сформированным объектом вызова, выбрасывается исключение {{jsxref("Global_Objects/TypeError", "TypeError")}}.

## Описание

В большинстве случаев метод `String.raw()` используется вместе с шаблонными строками. Первый синтаксис, показанный выше, используется редко, поскольку движок JavaScript будет вызывать метод с соответствующими аргументами, подобно другим [теговым функциям](/ru/docs/Web/JavaScript/Reference/template_strings#Tagged_template_strings).

Метод `String.raw()` является единственной встроенной теговой функцией шаблонных строк, выступающей стандартной функцией по объединению их фрагментов. Вы и сами могли бы реализовать подобную функциональность на JavaScript.

## Примеры

### Пример: использование метода `String.raw()`

```js
String.raw`Привет\n${2+3}!`;
// 'Привет\n5!', символ после 'Привет' не является символом новой строки,
// '\' и 'n' - это два символа.

String.raw`Привет\u000A!`;
// 'Привет\u000A!', а здесь мы получим символы
//  \, u, 0, 0, 0, A, всего 6 символов.
// Экранирующие символы не имеют особого значения и
// обратные слеши будут присутствовать в выходной строке.
// Вы можете убедиться в этом, проверив свойство .length строки.

let name = 'Боб';
String.raw`Привет\n${name}!`;
// 'Привет\nБоб!', сработала подстановка.

// Обычно вам не нужно вызывать метод String.raw() как функцию,
// но никто не запрещает вам делать это:
String.raw({ raw: 'тест' }, 0, 1, 2);
// 'т0е1с2т'
```

## Спецификации

{{Specifications}}

## Совместимость с браузерами

{{Compat}}

## Смотрите также

- [Шаблонные строки](/ru/docs/Web/JavaScript/Reference/template_strings)
- {{jsxref("Global_Objects/String", "String")}}
- [Лексическая грамматика](/ru/docs/Web/JavaScript/Reference/Lexical_grammar)
