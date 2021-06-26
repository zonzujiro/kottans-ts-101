---
theme: seriph
layout: image-right
image: https://images.unsplash.com/photo-1621112943521-775623b0f651?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=1534&q=80
class: "text-center"
highlighter: shiki

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

---
layout: image-right
image: https://dm1files.storage.live.com/y4mCoQWpJOraz62DCi1-WE75N4jA7Yl9wYGPoRAVY_7CdB7RnngpKcaI1k2aZkmUuOE2N5GSYpptlDtaM_FH6jh5m0zHgwXQpAT16j4qh_vIQ56teD_r8MLUs3jYAPWvco_Kg9t4ju9lAFz73tE3ICKFWmqSUqpmKNMDH8qY3BMsS6oCUdE6MgNUZilA1zF58Ph?width=3492&height=4656&cropmode=none
---

# Кто я?

## Ваня Титаренко

 💻 Team Lead в Wix

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

# Пока не начали

## Лекция большая - материала много

Так что давайте сделаем жизнь друг-друга немного удобнее

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

## Теория и совсем чуть-чуть практики

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
image: https://am3pap006files.storage.live.com/y4mTBVrNzHtdMrvw6jDsU-hJCfsmoaWiqaW3CFPCn8J8ZjuoyWT7GlMAPvHB25KmHwIDT3RAmlhvhdcuWPoGk3KkVFuBgVe6hCLLilvZBDhlOIE8IJ7eJj9WYDGLwDUsFPjYGdPodek7HicHmNeRgIFvfMPqcRyupsKglFBblYUJNjNxPrQjtWOkJENQuv_m9Oc?width=2529&height=2529&cropmode=none
---

# Женя: практика

- Расчитывает на то, что у вас будет база
- Расскажет как пользоваться Utility Types о которых расскажу я
- Еще более углубленно покажет то, как они работают
- И если все будет ок - решит пару интересных задач

<br>

# Погнали?

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
- Union and intersection types - `|` и `&`

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

Но в целом, как написали - так и работает

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
- нехватка стандартной библиотеки решается другими библиотеками - `mootools`, `jQuery`, `lodash`
- необходимость управления сложной логикой - фреймворками `Backbone`, `AngularJS`, `React` и т.п.
- а часть других проблем может решиться только типами - `TypeScript` и `Flow`

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

Я расскажу:

- `Pick<Type, Keys>` vs `Omit<Type, Keys>`
- `Exclude<Type, ExcludeUnion>` vs `Extract<Type, Union>`

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

Вам страшно?

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

Все! Вы знаете дженерики! Можно идти проситься на работу синьора-помидора! 💸

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
layout: statement
---

# Ща поплавит! 🤪
## Можем взять паузу минут на 10-15. М?

---

# Что делает функция?

```js
const unpacked = variable => {
  if (typeof variable === 'string') {
    return 'string';
  }

  if (Array.isArray(variable)) {
    if (onlyStrings(variable)) {
      return 'string';
    }

    if (onlyNumbers(variable)) {
      return 'number';
    }
  }

  if (typeof variable === 'function') {
    return typeof variable()
  }

  return typeof variable;
};
```

Тепло...

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

# Как думаете, что делает дженерик?

```ts
type T0 = Unpacked<string>; // string
type T1 = Unpacked<Array<string>>; // string
type T2 = Unpacked<() => string>; // string
type T3 = Unpacked<Promise<string>>; // string
type T4 = Unpacked<Array<Promise<string>>>; // Promise<string>
type T5 = Unpacked<Unpacked<Array<Promise<string>>>>; // string
```

Горячее...

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

# Реализация дженерика

## Тоже самое, но на TypeScript

```ts
type Unpacked<T> = T extends Array<string>
  ? string
  : T extends Array<number>
  ? number
  : T extends Promise<string>
  ? string
  : T extends Promise<number>
  ? number
  : T;
```

Удобно так писать?

```ts
type T0 = Unpacked<string>; // string
type T1 = Unpacked<Array<string>>; // string
type T2 = Unpacked<() => string>; // string
type T3 = Unpacked<Promise<string>>; // string
type T4 = Unpacked<Array<Promise<string>>>; // Promise<string>
type T5 = Unpacked<Unpacked<Array<Promise<string>>>>; // string
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

# Новое ключевое слово - *infer*

## BOOM! Магия TypeScript!

```ts
type Unpacked<T> = T extends Array<infer U>
  ? U
  : T extends (...args: Array<any>) => infer U
  ? U
  : T extends Promise<infer U>
  ? U
  : T;
```

Давайте подумаем 🤔

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

# Новое ключевое слово - *infer*

## TS, сам додумайся какой там тип...

```ts
type Unpacked<T> = T extends Array<infer U> // Если это массив - верни тип значения в массиве
  ? U
  : T extends (...args: Array<any>) => infer U // Если это функция - верни тип того, что она вернет
  ? U
  : T extends Promise<infer U> // ???
  ? U
  : T;
```
Первая строка говорит следующее:
> Если аргумент дженерика Т является расширением массива `<выгрызи тип из массива и запиши его в переменную U>`, верни U

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

# Итого

- `infer` - что-то вроде `typeof variable`, только для типов
- объявляет переменную и кладет в нее ее тип
- какую переменную туда класть и все такое - он "условно" решает сам
<br>
<br>

# Поняли? Или повторим?

> Если аргумент дженерика Т является расширением массива `<выгрызи тип из массива и запиши его в переменную U>`, верни U

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

# А теперь все вместе!

## ДЖЕ-НЕ-РИК!

```ts
type Unpacked<T> = T extends Array<infer U>
  ? U
  : T extends (...args: Array<any>) => infer U
  ? U
  : T extends Promise<infer U>
  ? U
  : T;

type T0 = Unpacked<string>; // string
type T1 = Unpacked<Array<string>>; // string
type T2 = Unpacked<() => string>; // string
type T3 = Unpacked<Promise<string>>; // string
type T4 = Unpacked<Array<Promise<string>>>; // Promise<string>
type T5 = Unpacked<Unpacked<Array<Promise<string>>>>; // string
```

IN-FER! УЗ-НАЙ ТИП САМ!

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

# Ну и последнее

## Mapped Types

```ts
interface IMyRecord {
  key1: number;
  key2: number;
  key3: number;
}
```

vs

```ts
type MyKeys = 'key1' | 'key2' | 'key3'

interface IMyRecord {
  [key: MyKeys]: number;
}
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

Обработаем событие 🙂

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

# И еще пример

## Same-same, but different

```ts
type Source = ???

const source1: Source = {
  firstProperty: 4,
  name: 'source',
  title: 'Record'
}

const source2: Source = {
  secondProperty: 4,
  name: 'source',
  title: 'Record'
}
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

# И еще пример

## Optional keys

```ts
type Source = {
  firstProperty?: number;
  secondProperty?: number;
  name: string;
  title: string;
}

const source1: Source = {
  firstProperty: 4,
  name: 'source',
  title: 'Record'
}

const source2: Source = {
  secondProperty: 4,
  name: 'source',
  title: 'Record'
}
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

# И еще пример

## Пересечение типов 🙂

```ts
type Source = {
  firstProperty: number;
  name: string;
  title: string;
} | {
  secondProperty: number;
  name: string;
  title: string;
}

const source1: Source = {
  firstProperty: 4
}

const source2: Source = {
  secondProperty: 4
}

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

# Summary example

## Get it done or die trying

```ts

type LeaveOnlyPrimitives = ???;

type StrippedMouseEvent = LeaveOnlyPrimitives<MouseEvent>;

// Dirty hack for learning purposes
const someStrippedMouseEvent = {} as StrippedMouseEvent;

someStrippedMouseEvent.initEvent(); // This expression is not callable. Type 'never' has no call signatures.
```

Что будем использовать - Union type, Mapped type, Conditional type, Generic, `extends`, `never`, `as`.

Жаль `infer` нет 🤪

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

# Die Hard

## Дженерик

```ts
type LeaveOnlyPrimitives<TEvent> = {};

type StrippedMouseEvent = LeaveOnlyPrimitives<MouseEvent>;

// Dirty hack for learning purposes
const someStrippedMouseEvent = {} as StrippedMouseEvent;

someStrippedMouseEvent.initEvent(); // This expression is not callable. Type 'never' has no call signatures.
```

Что дальше?

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

# Die Hard

## Тип аргумента - только Event

Расширения типа - `extends`

```ts
type LeaveOnlyPrimitives<TEvent extends Event> = {};

type StrippedMouseEvent = LeaveOnlyPrimitives<MouseEvent>;

// Dirty hack for learning purposes
const someStrippedMouseEvent = {} as StrippedMouseEvent;

someStrippedMouseEvent.initEvent(); // This expression is not callable. Type 'never' has no call signatures.
```

Что дальше?

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

# Die Hard

## Mapped type

Наше событие должно иметь те же свойства и значения, что и оригинал


```ts
type LeaveOnlyPrimitives<TEvent extends Event> = {
  [Property in keyof TEvent]: TEvent[Property]
};

type StrippedMouseEvent = LeaveOnlyPrimitives<MouseEvent>;

// Dirty hack for learning purposes
const someStrippedMouseEvent = {} as StrippedMouseEvent;

someStrippedMouseEvent.initEvent(); // This expression is not callable. Type 'never' has no call signatures.
```

Правильно?

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

# Die Hard

## Conditional type

Неправильно! Только примитивы

```ts
type LeaveOnlyPrimitives<TEvent extends Event> = {
  [Property in keyof TEvent]: TEvent[Property] extends string 
    ? TEvent[Property]
    : never
};

type StrippedMouseEvent = LeaveOnlyPrimitives<MouseEvent>;

// Dirty hack for learning purposes
const someStrippedMouseEvent = {} as StrippedMouseEvent;

someStrippedMouseEvent.initEvent(); // This expression is not callable. Type 'never' has no call signatures.
```

Это все?

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

# Die Hard

## Union Type

Ну и все, в принципе 😊

```ts
type Primitives = number | string | boolean;

type LeaveOnlyPrimitives<TEvent extends Event> = {
  [Property in keyof TEvent]: TEvent[Property] extends Primitives
    ? TEvent[Property]
    : never;
};

type StrippedMouseEvent = LeaveOnlyPrimitives<MouseEvent>;

// Dirty hack for learning purposes
const someStrippedMouseEvent = {} as StrippedMouseEvent;

someStrippedMouseEvent.initEvent(); // This expression is not callable. Type 'never' has no call signatures.
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

## Шоб от зубов отскакивало!

Медитируйте на ссылки:

- [Narrowing](https://www.typescriptlang.org/docs/handbook/2/narrowing.html)
- [Generic types](https://www.typescriptlang.org/docs/handbook/2/generics.html)
- [Utility type](https://www.typescriptlang.org/docs/handbook/utility-types.html)
- [Type inference](https://www.typescriptlang.org/docs/handbook/type-inference.html) и [Infer](https://www.typescriptlang.org/docs/handbook/release-notes/typescript-2-8.html#type-inference-in-conditional-types)
- [Conditional types](https://www.typescriptlang.org/docs/handbook/2/conditional-types.html)
- [Mapped types](https://www.typescriptlang.org/docs/handbook/2/mapped-types.html)

В начале лекции я говорил, что нужно знать для следующей - вы должны это знать.

Ну и все остальное о чем я тут говорил... 

Оооммм... 🧘

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