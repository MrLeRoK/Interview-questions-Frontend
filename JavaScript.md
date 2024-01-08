# JavaScript

<details>
    <summary>Типы данных</summary>

    null - содержит одно значение (null)
    undefined - означает, что значение не было присвоено
    boolean.
    number.
    string.
    object - хранят коллекции данных
    Символ (symbol) - примитивный тип данных,использующийся для создания уникальных идентификаторов.
 *   let in = Symbol("id")

    BigInt - позволяет работать с числами большой длинны

</details>


<details>
    <summary>Что такое Promise?</summary>

  _**Promise**_ — специальный объект JavaScript, который используется для написания и
  обработки асинхронного кода. Асинхронные функции возвращают объект Promise в качестве значения.
  Внутри промиса работает асинхронная операция, 
  которая управляет его состоянием. 

#### Промис может находиться в одном из трёх состояний: 

  - **pending** — промис ожидает, если результат не готов. То есть,
ожидает завершение чего-либо(например, завершения асинхронной операции).
  - **fulfilled** — получен результат; 
  - **rejected** — ошибка.

#### На promise можно навешивать колбэки двух типов:

* resolve – срабатывают, когда promise в состоянии «выполнен успешно».
* reject – срабатывают, когда promise в состоянии «выполнен с ошибкой».

#### Промис создаётся с помощью конструктора:
 > const promise = new **Promise**((resolve, reject) => {
  ...
  });

#### Методы объекта Promise
 - Promise.all() - используют, 
когда нужно запустить несколько промисов параллельно и дождаться их выполнения.
Возвращает массив значений всех переданных промисов, при этом сохраняя порядок оригинального (переданного) массива, но не порядок выполнения.

Пример: 

```js

const promise1 = new Promise(resolve => setTimeout(() => resolve(1), 5000))
const promise2 = new Promise(resolve => setTimeout(() => resolve(2), 2000))
const promise3 = new Promise(resolve => setTimeout(() => resolve(3), 1000))

Promise.all([promise1, promise2, promise3])
  .then(([response1, response2, response3]) => {
    console.log(response1)
    // 1
    console.log(response2)
    // 2
    console.log(response3)
    // 3
  })

```

</details>









