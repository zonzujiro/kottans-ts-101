---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
layout: image-right
image: https://images.unsplash.com/photo-1621112943521-775623b0f651?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1534&q=80
# apply any windi css classes to the current slide
class: "text-center"
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# some information about the slides, markdown enabled
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
---

<br>
<br>
<br>
<br>
<br>
<br>
<br>

# Advanced Types 101

Kottans TypeScript

<br>
<br>

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 p-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
    Весло, как символ того, что с TS вам придется разгребать все, что вы там себе <i>понапысювали</i><carbon:arrow-right class="inline"/>
  </span>
</div>


<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---
layout: image-right
image: https://dm1files.storage.live.com/y4mCoQWpJOraz62DCi1-WE75N4jA7Yl9wYGPoRAVY_7CdB7RnngpKcaI1k2aZkmUuOE2N5GSYpptlDtaM_FH6jh5m0zHgwXQpAT16j4qh_vIQ56teD_r8MLUs3jYAPWvco_Kg9t4ju9lAFz73tE3ICKFWmqSUqpmKNMDH8qY3BMsS6oCUdE6MgNUZilA1zF58Ph?width=3492&height=4656&cropmode=none
---

# Кто я?

## Ваня Титаренко

 💻 Frontend Developer в Wix

- 😼 Community lead в Kottans
- 💼 Бывший юрист
- 🏔 Люблю горы. Два раза был в Непале на высотах 5100 и 5400

<br>
<br>
<br>
<br>

### Никто на 16 дней в Перу не хочет в сентябре?


<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

---
layout: statement
---

# О чем поговорим?

В целом об инструментах которые есть в TS для создания своих типов

# О чем *не* поговорим

Обо **всех** типах и операторах, edgecases, usecases

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

---

# Правила

## Давайте сделаем жизнь друг-друга немного удобнее

- Что-то неясно? Можно и нужно перебить и задать вопрос
- Вопросы задавать лучше голосом - все хотят их услышать и понять, что "не я один не отстреливаю, что мне тут говорят"
- Кто не задает вопросы тот `<подставьте свое определение>`

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

---

# Я: вводная лекция

## Материала много - займет время

- Немного про JavaScript
- Немного о том, в кого TS "такой" и какой "такой"
- Немного о том почему нам надо писать свои типы и почему без этого никуда
- И это все чтобы подвести к Utility Types 
- И отправлю читать доку

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

---
layout: image-right
image: https://images.unsplash.com/photo-1621112943521-775623b0f651?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1534&q=80
---

# Женя: практика

- Как пользоваться Utility Types о которых я расскажу
- Расскажет более глубоко о том как они работают
- И если все будет ок - решит пару интересных задач

<br>

Погнали?

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

---

# Что вы должны знать

- Basic types - `number`, `string`, etc.
- `interface` vs `type`
- Union and intersection types

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

---

# Как будет работать этот кусок кода?

```js {all|2-6|5,13|3,10,14|2,10,15}
const users = [
  { name: 'Anastasiya', superPower: 'VJUH!!!', isKottan: true },
  { name: 'Elon Mask', suprePower: 'Smart', isKottan: false },
  { name: 'Khrystyna', superPower: 'Charming', isKottan: true },
  { name: 'Kottan', superPower: 'knowledge sharing', isKottan: 'absolutely!' },
  { name: 'Oleksiy', superPower: 'Management', isKottan: true },
];

function findByPower(users, superPower) {
  return users.find(user => user.superPower === superPower);
}

const kottans = users.filter(user => user.isKottan === true);
const smartPerson = findByPower(users, 'Smart')
const hasMagician = Boolean(findByPower(users, 'VJUH!!!').length);

```

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

---
layout: statement
---

# Не так как вы хотели!

## Но в целом, как написали - так и работает

<br>

```js
  { name: 'developer', superPower: 'wrote that code', isSmart: 'probably' },
```

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

---

# Почему JavaScript такой?

## Изначально - язык для домохозяек

Для этого он должен быть **прощающим** и гибким
- `falsy` и `truthy` значения
- конвертация типов - `==`, `===`, `!!`
- на старте только простые ментальные модели - никаких промисов!!!
- и т.п.

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

---

# Почему JavaScript такой?

## Потом уже для крутых разработчиков

Время шло, задачи и проблемы становились сложнее:
- часть из них решалась библиотеками - mootools, jquery, lodash
- часть фреймворками - Backbone, AngularJS, React
- а часть может решиться только типами - TypeScript и Flow

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

---

# Ну ок. А TypeScript какой?

## Не читает мысли, а как описали типы - так и работает

TypeScript работает по принципу Types First - не смотрит на сам код, а смотрит в основном только на типы

```ts
const elem = document.getElementById('#my-id'); // null | Element

if (elem !== null) {
  return
}

elem.classList.add('classname') // Element may be null
```

TS все равно выводил ошибку несмотря на наличие проверки. Сейчас уже не так из-за наличия `type guard` и `control flow analysis`

> [Flow](https://flow.org/) пытался понимать ход исполнения программы и быть "типизацией без необходимости написания типов". Но не срослось - долгое время проверки, частые false positive ошибки, отстутствие документации и типов для сторонних библиотек. Сейчас говорят получше стало


<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

---

# Ну ок. А TypeScript какой?

## TypeScript - тот еще фантазер

Будет пытаться додумывать, там где это возможно

```ts
function sum(a: number, b: number): number {
  return a + b;
}

const result = sum(1, 2);
```

vs

```ts
function sum(a: number, b: number) {
  return String(a) + b;
}

const result = sum(1, 2); // typeof result === 'string'
```

A где невозможно - молча вставит `any` и не будет проверять 👌

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

---
layout: statement
---

# Ну и будет раздражать

## Я **знаю** что оно работает именно так, а TypeScript не понимает! ЪУЪ TypeScript!!!

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

---

# А TypeScript такой почему?

## Из-за JavaScript и нас с вами!

JavaScript сам по себе натура ветренная, динамичная и на этапе проектирования в нем не подразумевалась декларация типов.

> Проверку типов хотели встроить в ES3 (???) версии, но не стали дабы не усложнять

Соответственно было целое сообщество разработчиков, которое типы не видело в глаза, но кода написало на весь интернет.

Соответственно, в отличии от шарпов, джавы и т.п., он может накатываться вокруг существующего проекта в котором типизации нет, все работает на вжухах и принципе "я знаю, что оно именно так работает".

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

---
layout: statement
---

# Гибкая система типизации
## которая не будет давать стрелять себе в ногу и не закошмарит разработчика в процессе

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>
---

# Utility types

## Но не все, а только интересные 😹

- `Pick<Type, Keys>` vs `Omit<Type, Keys>`
- `Exclude<Type, ExcludeUnion>` vs `Extract<Type, Union>`
- `Partial<Type>`
- `Readonly<Type>`

## Неинтересные - легко поймете после интересных

`ThisType<Type>`, `NonNullable<Type>`, `Parameters<Type>`, `ConstructoParameters<Type>`, `InstanceType<Type>`, `ThisParameterType<Type>`, `OmitThisParameter<Type>`, `Uppercase<StringType>`, `ReturnType`, etc.

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>
---

# И немного еще

- Generics 101
- `Record<Keys, Type>`
- `typeof` vs `keyof`

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

---
layout: statement
---

# Generics - функции для создания других типов

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

---

# Generics

## То, чего все почему-то боятся

```ts
const pick = (source: Record<string, any>, keys: Array<string>) => {
  const result = []

  keys.forEach(key => {
    if (key in source) {
      result.push(source[key])
    }
  })

  return result
}

const source = {
  kottan: 'mascot',
  anastasiya: 'VJUH!!!',
  nikita: 'framework-power'
}

const result = pick(source, ['nikita', 'anastasiya']) // ???
```

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>
---

# Generics

## А теперь с массивами

```ts
const exclude = (source: Array<string>, toExclude: Array<string>) => {
  return source.filter(item => !toExclude.includes(item))
}

const source = ['nikita', 'anastasiya', 'mascot']
const result = exclude(source, ['nikita', 'anastasiya']) // ???
```

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

---

# А теперь тоже самое, но с типами

## `Omit` - функция обратная `Pick`

Дженерики получают аргументы и возвращают результат

```ts
interface ISource {
  kottan: 'mascot';
  anastasiya: 'VJUH!!!';
  nikita: 'framework-power';
}

type Picked = Pick<ISource, 'nikita' | 'anastasiya'> // { nikita: 'framework-power'; anastasiya: 'VJUH!!!' }
type Omitted = Omit<ISource, 'nikita' | 'anastasiya'> // ???
```

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

---

# А теперь тоже самое, но с типами

## `Exclude` vs `Extract`

В начале не понял, а потом как понял 🙀

```ts
type Source = 'nikita' | 'anastasiya' | 'mascot'
type Excluded = Exclude<Source, 'nikita' | 'anastasiya'> // 'mascot'
type Extracted = Extract<Source, 'nikita' | 'anastasiya'> // ???
```

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

Все! Вы знаете дженерики! Можно идти проситься на работу синьора! 💸

---
layout: statement
---

# Идея ясна?

## Поехали дальше!

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

---

# Мы можем писать свои дженерики

## Собственно, в этом их основная сила

```ts
type IsString<TArgument> = TArgument extends string ? TArgument : never;

type MaybeString = IsString<'string'>
type MaybeString2 = IsString<true>
```

В этом примере использованы:

- `extends` - значение должно **расширять** тип строки
- `conditional type` - типа тернарный оператор (шутка за 300)
- `never` - означает, что мы не хотим работать с результатами этих вычислений

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

---

# Мы можем писать свои дженерики

## Код невероятной сложности

```ts
type IsStringOrNumber<TArgument> = TArgument extends string
  ? TArgument
  : TArgument extends number
  ? TArgument
  : never;

type MaybeNumber = IsStringOrNumber<1>;
```

Есть идеи?

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

---

# Еще немного...

## Можно указать тип для аргумента

```ts
const sum = (a: number, b: number) => { ... };
type Sum<Ta extends number, Tb extends number> = ...;

Sum<'1', '2'> // Error!
```

## Можно задать значение по умолчанию

```ts
const sum = (a: number = 2, b: number = 2) => { ... };
type Sum<Ta extends number = 2, Tb extends number = 2> = ...; 

type Result = Sum; // Maybe4 :D
```

Вроде ничего сложного?

> Пример на самом деле немного кривой - не надо использовать конкретные значения в типах

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

---
layout: statement
---

# Пока что было легко
## Ща жара пойдет. Готовы? 😎

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

---

# Generics AND functions!

TypeScript, исходя из типа указанного в декларации функции, понимает какие типы аргументов может принимать ваша функция

```ts
function isString<TMaybeString>(maybeString: TMaybeString) {
  return typeof maybeString === 'string';
}

const stringType = isString('1'); // function isString<string>(maybeString: string): boolean
const numberType = isString(2); // function isString<number>(maybeString: number): boolean
```

Можно указать тип по умолчанию:

```ts
function isString<TMaybeString extends number>(maybeString: TMaybeString) ...

const stringType = isString('1'); // Болбес? Ошибка же
```

Вопрос с подвохом - как указать тип значения по умолчанию для аргумента?

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

---

# inferring

## `typeof` но на типах

```ts
const typeOfString = typeof 'string'
type TypeOfString<infer P> = 
```

---
layout: statement
---

# Постепенно закругляемся
## И разбираем примеры

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

---

# Пример

## Закрепить, так сказать

Oldy, but goody

```ts
declare function fetch(input: RequestInfo, init?: RequestInit): Promise<Response>;
```

Новички на ринге:

- `declare` 
- `Promise`
- `?`

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

---

# Еще пример

## Следующий

Обработаем событие :)

```ts
interface DocumentEventMap {
    "scroll": MouseEvent;
    "click": MouseEvent;
    "change": Event;
    // ...
}

addEventListener<K extends keyof DocumentEventMap>(type: K, listener: (this: Document, ev: DocumentEventMap[K]) => any, options?: boolean | AddEventListenerOptions): void;
```

Новички на ринге:

- `keyof`

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

---
layout: statement
---

# Пока что все. Задавайте вопросы
## А потом домашку дам

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

---

# Домашнее задание

## Шоб от зубов отскакивало

- [generic types](https://www.typescriptlang.org/docs/handbook/2/generics.html)
- [utility type](https://www.typescriptlang.org/docs/handbook/utility-types.html)
- inferring
- mapped types 
- [conditional types](https://www.typescriptlang.org/docs/handbook/2/conditional-types.html)
- и все остальное о чем я тут говорил - [`keyof`](https://www.typescriptlang.org/docs/handbook/2/keyof-types.html)

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

---