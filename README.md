# Проект

> [Требования](https://praktikum.notion.site/74dd6e68fda34387ac4d43137a601c6e) и [макеты(figma)](https://www.figma.com/design/aPMo2hRx5qxLm6vkr9ZUBw/%D0%AF%D0%BD%D0%B4%D0%B5%D0%BA%D1%81.%D0%9C%D0%B0%D1%80%D1%88%D1%80%D1%83%D1%82%D1%8B-(Copy)?node-id=2-18586&p=f&t=1T7KprBuT9PhY1Vp-0)


## Задачи

### 1. Подготовить чек-лист на вёрстку полей

**Составить чек-лист на вёрстку:**

- один тариф формы бронирования
- разные состояния полей «Добавить права» и «Способ оплаты»
- элементы на навигационной карте: это иконки автомобилей и действия с ними
- Окна «Машина забронирована», «Вы уверены, что хотите отменить поездку?» и «Поездка отменена» 

**Не включать в проверки:**

-  Валидацию полей
- Окна «Добавление прав», «Способ оплаты», «Добавление карты»

### 2. Подготовить чек-лист и тест-кейсы на логику работы окон

**Составить тестовую документацию:** 

- чек-лист на логику окон «Способ оплаты» и «Добавление карты»,
- тест-кейсы на кнопку «Забронировать»

**Не включать в документацию:**

- Расчёт расстояния и времени в пути

### **3. Протестировать приложение и завести баг-репорты**

1. **Вёрстка в окружениях:** 
   - Яндекс Браузер, разрешение экрана 800×600;
   - Firefox, разрешение экрана 1920×1080.
2. **Логика в  одном из окружений выше**

> В требованиях сказано, что после заполнения поля «Добавить права» включается таймер на 30 секунд. В текущей реализации его **нет**. Разработчики специально переделали тестовый стенд: так не придётся ждать каждый раз, когда выполняется проверка  

### 4. Подвести итоги


## Тестовая документация

**[1. Чек-лист на вёрстку](https://docs.google.com/spreadsheets/d/1vPbPya69ZvNRhwItrgrwepQ0gSoQfxeY_smRZAXZhh8/edit?gid=899462569#gid=899462569)**

**[2. Чек-лист «Способ оплаты» и «Добавление карты»](https://docs.google.com/spreadsheets/d/1vPbPya69ZvNRhwItrgrwepQ0gSoQfxeY_smRZAXZhh8/edit?gid=1540435533#gid=1540435533)**

**[3. Тест-кейсы на кнопку «Забронировать»](https://docs.google.com/spreadsheets/d/1vPbPya69ZvNRhwItrgrwepQ0gSoQfxeY_smRZAXZhh8/edit?gid=1567345705#gid=1567345705)**

**[Баг-репорты](https://docs.google.com/spreadsheets/d/1vPbPya69ZvNRhwItrgrwepQ0gSoQfxeY_smRZAXZhh8/edit?gid=977751969#gid=977751969)**


## Итоги

### Объекты тестирования

Полностью покрыта тестами верстка формы бронирования авто в формате каршеринга для выбора тарифа “Повседневный”, иконки авто на карте и окно “Машина забронирована”. Также удалось проверить логику работы привязки карт и валидацию полей связанных с процессом оплаты бронирования авто и бронирования авто в целом.  

### Результаты

Все тесты по верстке выполнены за исключением проверок части элементов интерфейса процесса верификации прав в связи с его отсутствием [BUG-6](https://docs.google.com/spreadsheets/d/1vPbPya69ZvNRhwItrgrwepQ0gSoQfxeY_smRZAXZhh8/edit?gid=977751969#gid=977751969&range=7:7) , окон отмены заказа, к которым нет доступа [BUG-14](https://docs.google.com/spreadsheets/d/1vPbPya69ZvNRhwItrgrwepQ0gSoQfxeY_smRZAXZhh8/edit?gid=977751969#gid=977751969&range=15:15) и отображением стартовой цены тарифа / времени в пути до забронированного авто из-за блокирующего бага [BUG-36](https://docs.google.com/spreadsheets/d/1vPbPya69ZvNRhwItrgrwepQ0gSoQfxeY_smRZAXZhh8/edit?gid=977751969#gid=977751969&range=37:37).

Есть довольно критичный баг с окном бронирования авто на планшетах [BUG-12](https://docs.google.com/spreadsheets/d/1vPbPya69ZvNRhwItrgrwepQ0gSoQfxeY_smRZAXZhh8/edit?gid=977751969#gid=977751969&range=13:13) и [BUG-13](https://docs.google.com/spreadsheets/d/1vPbPya69ZvNRhwItrgrwepQ0gSoQfxeY_smRZAXZhh8/edit?gid=977751969#gid=977751969&range=14:14), не позволяющий узнать что ты забронировал. Иконки авто на карте не работают [BUG-16](https://docs.google.com/spreadsheets/d/1vPbPya69ZvNRhwItrgrwepQ0gSoQfxeY_smRZAXZhh8/edit?gid=977751969#gid=977751969&range=17:17) - [BUG-21](https://docs.google.com/spreadsheets/d/1vPbPya69ZvNRhwItrgrwepQ0gSoQfxeY_smRZAXZhh8/edit?gid=977751969#gid=977751969&range=22:22), здесь нужно много доработок. Остальные баги вёрстки некритичные или малозначительные, доступны по ссылке на все баг-репорты.

После тестирования логики привязки банковских карт обнаружился критический, баг затрудняющий использование банковских карт в приложении [BUG-26](https://docs.google.com/spreadsheets/d/1vPbPya69ZvNRhwItrgrwepQ0gSoQfxeY_smRZAXZhh8/edit?gid=977751969#gid=977751969&range=27:27) - сложно понять какой конкретно картой пользуешься. Также есть проблемы с использованием нескольких карт [BUG22](https://docs.google.com/spreadsheets/d/1vPbPya69ZvNRhwItrgrwepQ0gSoQfxeY_smRZAXZhh8/edit?gid=977751969#gid=977751969&range=23:23) и [BUG25](https://docs.google.com/spreadsheets/d/1vPbPya69ZvNRhwItrgrwepQ0gSoQfxeY_smRZAXZhh8/edit?gid=977751969#gid=977751969&range=26:26).

Бронирование авто невозможно отменить [BUG-14](https://docs.google.com/spreadsheets/d/1vPbPya69ZvNRhwItrgrwepQ0gSoQfxeY_smRZAXZhh8/edit?gid=977751969#gid=977751969&range=15:15)! И еще мы вводим в заблуждение пользователя неработающим вызовом окна [BUG34](https://docs.google.com/spreadsheets/d/1vPbPya69ZvNRhwItrgrwepQ0gSoQfxeY_smRZAXZhh8/edit?gid=977751969#gid=977751969&range=35:35), что тоже не есть хорошо. А забронировать авто и вовсе возможно без какой-либо оплаты [BUG35](https://docs.google.com/spreadsheets/d/1vPbPya69ZvNRhwItrgrwepQ0gSoQfxeY_smRZAXZhh8/edit?gid=977751969#gid=977751969&range=36:36)!!!

Остальные баги логики оплаты и бронирования не такие срочные и тоже доступны по ссылке на все баг-репорты.

### Вывод

Такой продукт в релиз выпускать не*льзя. Есть неработающие области в вёрстке и с этим приложением еще можно как-то пользоваться. Но неработающая верификация прав, сложности с использованием карт и дыры в безопасности процесса бронирования авто не позволяют выпустить продукт в релиз.  
