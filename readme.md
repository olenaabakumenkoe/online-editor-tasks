# online-editor-tasks

## Install

Для запуску необхідно встановити залежності, виконавши 
команду `npm install` в корні проекту.

Вимоги до версій "Nodejs" та "npm":

```json
{
  "node": ">=16.0.0",
  "npm": ">=8.0.0"
}
```

## Структура задачі

До проекту задачі додаються шляхом пулл-реквесту в поточний репозиторій.

  ```
  .
  └── 📁 00-taskName
    ├── 📄 readme.md
    ├── 📄 index.js
    ├── 📄 index.spec.html
    ├── 📄 index.spec.js
    └── 📁 solution
        ├── 📄 index.js
        └── 📄 readme.md
  ```
  
  * **_readme.md_** - опис завдання
  * **_index.js_** - структура завдання без рішення
  * **_index.spec.html_** - файл для запуску тестів
  * **_index.spec.js_** - тести до завдання
  * **_solution/index.js_** - файл з розв'язанням завдання
  * **_solution/readme.md_** - опис алгоритму розв'язання завдання

## Структура треку завдань

Трек (track) - це підбірка завдань/задач об'єднаних спільною ідеєю.

Можна об'єднувати задачі в трек за критерієм складності, наприклад:

* "js-core-level-1"
* "js-core-level-2"
* "js-core-level-3"
* ...

Так само можна піти шляхом об'єднання завдань відповідно до тем:

* "array-methods"
* "data-conversion"
* "objects"
* "algorithms"
* ...

Або навіть об'єднати ці два підходи: "array-methods-level-1"

Кожен track може містити до 99 задач, які іменуються за відповідним шаблоном:

```
<номер-завдання>-<назва-завдання>
```

**Приклад:**

  ```
  .
  └── 📁 trackName
    ├── 📄 readme.md
    ├── 📁 01-taskName
    ├── 📁 02-someTask
    ├── 📁 ... 
    ├── 📁 99-anotherTask
  ```

  * **_readme.md_** - опис треку
  * **_00-taskName_** - назва завдання
  
Самі завдання будуть видаватись користувачу для вирішення відповідно до номера в
назві завдання.

## Запуск тестів

Для тестування завдань використовується ["jasmine"](https://github.com/jasmine/jasmine).
Тести до завдань можна запустити двома способами:

* відкривши в браузері файл **_"index.spec.html"_** відповідного завдання 
* запустивши одну з команд тест-ранера ["karma"](https://karma-runner.github.io/latest/index.html)

### Запуск тестів за допомогою Karma

Запуск тестів для всіх треків:

```
npm run test:karma
```

Запуск тестів для певного завдання:

```
npm run test:karma -- --grep <track-name>/<test-name>
```

Наприклад запустимо тести для задачі "sum" в треку "basic":
`npm run test:karma -- --grep basic/sum`

Запуск тестів для всього треку:

```
npm run test:karma -- --grep <track-name>
```

Наприклад запустимо для всього треку `basic`:
`npm run test:karma -- --grep basic`

## Як додати трек?

Для того щоби додати трек, необхідно в директорії **_"tracks"_** створити директорію з
назвою треку, наприклад "array-methods" та додати в цю директорію файл "readme.md" 
з описом треку.

```
  .
  └── 📁 tracks
    ├── 📁 ... 
    ├── 📁 array-methods
        ├── 📄 readme.md
    ├── 📁 ... 
```

## Як додати завдання?

Завдання або задачі можна додавати як в наявні треки, так і створювати нові треки з
завданнями.

Кожна задача має відповідати структурі описаній в розділі [Структура задачі:](#структура-задачі)

Приклад структури задачі знаходиться в директорії ["_task-example"](./_task-example)
