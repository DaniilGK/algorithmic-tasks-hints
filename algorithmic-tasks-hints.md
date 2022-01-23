# Советы по подготовке к выполнению алгоритмических задач.

## Установка Node.js.

Для начала нужно установить Node.js. Скачать дистрибутив можно с официального сайта: https://nodejs.org/ru/ .

![Node.js](./img/01.png "Сайт Node.js")

Рекомендую качать версию LTS(Long-Term Support или длительный срок поддержки). Если вам нужна другая версия, то нажмите на "Другие загрузки" или перейдите по ссылке https://nodejs.org/ru/download/ .

Во время установки не рекомендую ничего менять.

![Install Node.js](./img/02.png "Установка Node.js")
![Install Node.js](./img/03.png "Установка Node.js")
![Install Node.js](./img/04.png "Установка Node.js")
![Install Node.js](./img/05.png "Установка Node.js")
![Install Node.js](./img/06.png "Установка Node.js")
![Install Node.js](./img/07.png "Установка Node.js")
![Install Node.js](./img/08.png "Установка Node.js")

NPM устанавливается вместе с Node.js.


## Выполнение алгоритмических задач.

Для начала нужно перейти на страницу задачи. Для примера задача **Human Readable Number**:

![HRN](./img/09.png "Human Readable Number")

Перейдите на GitHub репозиторий задачи и сделайте его форк себе, нажав на кнопку **Fork**:

![HRN](./img/10.png "Human Readable Number")

Затем клонируйте себе на компьютер репозиторий:

![HRN](./img/11.png "Human Readable Number")

```bash
git clone git@github.com:UserName/human-readable-number.git
```
Где UserName - ваш ник на GitHub.
После клонирования перейдите в директорию задачи коммандой:
```bash
cd human-readable-number
```
![HRN](./img/12.png "Human Readable Number")

И установите зависимости:
```bash
npm install
```
![HRN](./img/13.png "Human Readable Number")

Красным выделенно сообщение **For this task we are strictly recomend you to use node <=12. Now you are using node v16.13.2, if you are using any of features that not supported by node <=12, score won't be submitted** говорящее о том, что рекомендуют использовать Node.js с версией меньше или равной 12. Если не использовать методы появившиеся в Node.js позже 12 версии - это не критично. Как узнать в какой версии появилась поддержка того или иного метода будет показано в конце статьи.

## Процесс работы с репозиторием задачи.

Ваше решение задачи нужно записать в файл `index.js` в директории `src`, строго в данной там функции:
```js
module.exports = function toReadable (number) {
  
}
```

Это нужно для работоспособности тестов и автотеста в рсапп.

Для запуска тестов запустите в терменале:
```bash
npm test
```
![HRN](./img/14.png "Human Readable Number")

Результат успешных тестов будет такой:

![HRN](./img/15.png "Human Readable Number")

Если тесты не прошли - то такой:

![HRN](./img/16.png "Human Readable Number")

Где **Should return 'one' when 1** говорит о том, что тест ожидает получить **one** если на входе **1**. **undefined** **==** **'one'**: **undefined** - что ваш код выдает, **'one'** - что тест ожидает.

После того как вы решите задачу и все тесты будут проходить успешно не забудьте запушить изменения на GitHub.

## Как узнать в какой версии появилась поддержка того или иного метода.

Наберите название метода в поисковой системе, например Google, и перейдите на сайт MDN (Mozilla Developer Network):

![HRN](./img/17.png "Human Readable Number")

Опуститесь в низ страницы до раздела **Совместимость с браузерами**:

![HRN](./img/18.png "Human Readable Number")

Крайняя правая колонка показывает начиная с какой версии Node.js началась поддержка данного метода.