## Що таке Node Version Manager (NVM)?
**Node Version Manager** - це це утиліта що дозволяє без проблем перемикатися між різними версіями Node. Ви можете встановити будь-яку версію однією командою і встановити версію за замовчуванням через інтерфейс командного рядка.

## Які ж операційні системи підтримує NVM?
NVM був спочатку розроблений для Linux і OS X, але також існує проект NVM Windows https://github.com/coreybutler/nvm-window. Хоча існують незначні відмінності, базові команди для установки, перегляду і перемикання версій Node.js ідентичні, крім випадків описаних нижче.

## Встановлення NVM на MacOS та Linux
Перш за все, переконайтесь в тому що утиліта сумісна з вашою версією операційної системи. Також технічно вам не потрібно видаляти вже встановлений Node, але краще зробити це, крім того, потрібно видалити будь-які колишню версію npm.
Але, C ++ компілятор необхідний для підтримки версій попередній 0.8.6. Навіть якщо ви зазвичай працюєте тільки з LTS або більш сучасними релізами, ви все ще можете встановити компілятор C ++. 

**Якщо ви у вас OS X, ваш кращий вибір це Xcode. Щоб встановити його виконайте наступну команду:**
```xcode-select --install```

**Якщо ви використовуєте Linux, виконайте наступну команду, щоб встановити build-essential package разом з Advanced Package Tool:**
```sudo apt-get update```
```sudo apt-get install build-essential```
 
 **Після цього, ви можете встановити Node Version Manager використовуючи cURL:**
 
 ```curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.33.11/install.sh | bash```
 
## Встановлення NVM на Windows
 Перед тим як ви почнете, видаліть існуючу версію Node.js, щоб уникнути потенційних проблем під час установки. Далі скачайте з Github ```nvm-setup.zip``` *https://github.com/coreybutler/nvm-windows/releases* після того як відкриєте його, просто дотримуйтесь інструкцій для завершення встановлення.
 ![image](https://user-images.githubusercontent.com/66551575/115295280-3ef45900-a162-11eb-82d4-f63ef197d588.png)

## Встановлення різних версій Node.js
 Менеджер версій робить установку різних версій Node.js дуже простою за допомогою однієї команди. Просто запустіть команду *install* і передайте їй параметром необхідну версію. Наприклад, якщо ви хочете встановити Node.js версії v6.5.0, виконайте наступну команду:
 
 ```nvm install v6.5.0```
 
 Так як утиліта має SemVer, ви можете встановлювати патчі командою *install* з аргументом номера патча. Для отримання списку доступних версій в Linux і OS X, виконайте:
 
 ```nvm ls-remote```
 
 **Якщо ви використовуєте Windows, запустіть таку команду:**
 
 ```nvm ls available```
 
 **Якщо вам потрібно видалити екземпляр Node, просто виконайте** ```nvm uninstall``` **c потрібним номером версії.**
 
## Глобальні NPM пакети
 Варто зауважити, то що глобально встановлені ```npm пакети``` не розділяються між різними версіями Node.js, тому що вони можуть заподіяти проблеми несумісності. Тому, Node Version Manager одночасно встановлює сумісну версію npm кожен раз коли ви встановлюєте якусь версію Node.js. Так як кожен екземпляр Node має власну версію npm, ви можете запустити ```npm -v``` що-б перевірити поточну версію зараз використовується. Також не потрібно мати ```sudo``` права при установці глобальних пакетів. Якщо ви хочете перевстановити глобальні npm пакети для певної версії Node.js або при її установці, зробіть так:
 
 ```
 nvm install v6.5.0 --reinstall-packages-from=4.2
 ```
 
 Команда вище встановлює Node 6.5.0 і необхідну npm, потім перевстановлює все встановлене в версії 4.2
 
## Аліас
 Що полегшити процес зміни версій, NVM дозволяє використовувати псевдоніми для визначення версій без вказівки номера. Приклади стандартних алиасов:
  * node: встановлює найостаннішу стабільну версію Node.js
  * unstable: встановлює найостаннішу стабільну версію Node.js
  * iojs: встановлює найостаннішу стабільну версію io.js
 
 **Для встановлення останньої стабільної версії Node.js виконайте наступну команду:**
  
  ```nvm install node```
  
 **Також існує алиас за замовчуванням. Для установки версії за умовчанням використовуйте таку команду:**
 
 ```nvm alias default node```
 
 **Для видалення аліаса, виконайте команду unalias:**
 
 ```nvm unalias with-async-await```
 
 **Переключення між версіями Node.js**
 
 Щоразу як ви встановлюєте нову версію Node.js, вона буде автоматично вибиратися для використання. Для перемикання між версіями використовується команда, nvm use яка працює майже так само як і команда install. Наприклад якщо ви хочете перейти на останню стабільну версію, виконайте команду:
 
 ```nvm use node```
 
 Для отримання списку всіх встановлених версій Node, використовується команда **nvm ls**:
 
 ```nvm ls```
 
## Додаткові команди
 * Існує кілька додаткових команд, які можуть вам коли-небудь знадобитися. Щоб запустити команду для встановленої версії без перемикань змінних node, використовуйте такий формат:
 
 ```nvm run 8.11.4 --version```
 
 * Щоб задати певну версію при запуску команда в саб-терміналі, виконайте таку команду:
 
 ```nvm exec 8.11.4 node --version```
 
 * Якщо ви хочете дізнатися шлях до виконуваних файлів Node.js для якоїсь версії Node, використовуйте наступний формат:
 
 ```nvm which 8.11.4```

## Переваги використання Node Version Manager
 
 Крім економії часу і зусиль, можливість перемикання між версіями Node має ще кілька значних вигод. Наприклад, якщо ви хочете перевірити роботу деякого пакета на певній версії Node, або якщо вам потрібно відтворити баг на потрібної версії, NVM дозволяє швидко переключитися і зробити налагодження.
 
 
### Учасники:

Кучеренко Іван 

### Контактні дані:
 - [Телеграм](http://t.me/rmnstepaniuk)

## Посилання на репозиторій
 - [GitHub](https://github.com/IKu4er/-Node.js-Server-Platform)
 
 
 
 
 
 
 
 
