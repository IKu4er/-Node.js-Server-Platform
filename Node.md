## Node.js
Node.js - це серверна платформа для роботи з JavaScript через движок V8. JavaScript виконує дію на стороні клієнта, а Node - на сервері. За допомогою Node можна писати
повноцінні програми. Node вміє працювати з зовнішніми бібліотеками, викликати команди з коду на JavaScript і виконувати роль веб-сервера.

## Переваги застосування Node.js:
  * **Простий і широко відомий JavaScript** Звичайно, платформа передбачає власні інструменти та особливості, наприклад, тут немає браузерних API, coockie або DOM, зате присутні
власні бібліотеки та інші цікаві рішення. Але в основному використовуються можливості і синтаксис всім звичного JavaScript.
  * **Багата стандартна бібліотека.** Платформа від самого початку має широкий набір можливостей, а в нових версіях бібліотека поповнюється і поліпшується.
  * **Величезне зовнішніх бібліотек і готових модулів.** Використання пакетного менеджера NPM дозволяє постійно розвивати екосистему Node. Сьогодні число опенсорсних пакетів в ньому перевалило за цифру 500 тисяч і постійно зростає.
  * **Движок V8** JavaScript створювався як інтерпритована скриптова мова. Але процес його інтерпретації не настільки швидкий і простий, як хотілося б. При цьому мова розвивається, він давно став повноцінним, на JavaScript можна писати великі програми. А тому наявність компілятора стало не просто плюсом, але - необхідністю.
## Збірка Node.js
Після того, як ви створили двійковий файл, наступним кроком буде запуск набору тестів, щоб переконатися, що двійковий файл працює належним чином.
Сервер на Node ніколи не виявиться набагато могутнішим, ніж потрібно. Модульність Node дозволяє створювати маленькі додатки, не стикаючись при цьому з необхідністю 
підтримки величезної інфраструктури, багато частин якої в якомусь конкретному випадку виявляється не задіяними. При розробці Node-додатків програміст вибирає саме те, 
що йому потрібно, і, при необхідності, розширює рішення.

## Рівні підтримки 
* **Рівень 1** : Ці платформи представляють більшість користувачів Node.js. Робоча група по збірці Node.js підтримує інфраструктуру для повного тестування. 
Помилки тестування на платформах рівня 1 блокують випуски.
* **Рівень 2** : Ці платформи представляють менші сегменти бази користувачів Node.js. Робоча група збірки Node.js підтримує інфраструктуру для повного охоплення тестів. Невдалі тести на платформах рівня 2 блокують випуски. Проблеми з інфраструктурою можуть затримати випуск бінарних файлів для цих платформ.
* **Експериментальна** : Може не компілюватися або набір тестів може не пройти. Основна команда не створює релізів для цих платформ. Збої тестів на експериментальних платформах не блокують випуски. Вітаються вклади в поліпшення підтримки цих платформ.

## Список платформ:
Підтримка компіляції / виконання Node.js залежить від операційної системи, архітектури та версії libc. У таблиці нижче вказано рівень підтримки для кожної підтримуваної комбінації. Список підтримуваних наборів інструментів для компіляції також надається для платформ рівня 1.
Node.js не підтримує версію платформи, якщо у постачальника закінчився термін її підтримки. Іншими словами, Node.js не підтримує роботу на платформах з вичерпаним терміном експлуатації(EoL).![image](https://user-images.githubusercontent.com/66551575/112995964-6dd76a80-9174-11eb-8124-5d2498cca63b.png)

| Операційна система | Архітектура    | Версії                            | Тип підтримки | Помітки                             |
| ----------------   | ---------------- | ------------------------------- | ------------  | --------------------------------- |
| GNU/Linux          | x64              | kernel >= 3.10, glibc >= 2.17   | Рівень 1        | e.g. Ubuntu 16.04 <sup>[1](#fn1)</sup>, Debian 9, EL 7 <sup>[2](#fn2)</sup> |
| GNU/Linux          | x64              | kernel >= 3.10, musl >= 1.1.19  | Експериментальний | e.g. Alpine 3.8                   |
| GNU/Linux          | x86              | kernel >= 3.10, glibc >= 2.17   | Експериментальний | Downgraded as of Node.js 10       |
| GNU/Linux          | arm64            | kernel >= 4.5, glibc >= 2.17    | Рівень 1       | e.g. Ubuntu 16.04, Debian 9, EL 7 <sup>[3](#fn3)</sup> |
| GNU/Linux          | armv7            | kernel >= 4.14, glibc >= 2.24   | Рівень 1       | e.g. Ubuntu 18.04, Debian 9       |
| GNU/Linux          | armv6            | kernel >= 4.14, glibc >= 2.24   | Експериментальний | Downgraded as of Node.js 12       |
| GNU/Linux          | ppc64le >=power8 | kernel >= 3.10.0, glibc >= 2.17 | Рівень 2       | e.g. Ubuntu 16.04 <sup>[1](#fn1)</sup>, EL 7  <sup>[2](#fn2)</sup> |
| GNU/Linux          | s390x            | kernel >= 3.10.0, glibc >= 2.17 | Рівень 2       | e.g. EL 7 <sup>[2](#fn2)</sup>    |
| Windows            | x64, x86 (WoW64) | >= Windows 8.1/2012 R2          | Рівень 1       | <sup>[4](#fn4),[5](#fn5)</sup>    |
| Windows            | x86 (native)     | >= Windows 8.1/2012 R2          | Рівень 1 (running) / Experimental (compiling) <sup>[6](#fn6)</sup> | |
| Windows            | x64, x86         | Windows Server 2012 (not R2)    | Експериментальний |                                   |
| Windows            | arm64            | >= Windows 10                   | Рівень 2 (compiling) / Experimental (running) |    |
| macOS              | x64              | >= 10.13                        | Рівень 1       |                                   |
| macOS              | arm64            | >= 11                           | Експериментальний |                                   |

* GCC 8 не входить в базову платформу. Користувачам знадобиться devtoolset-8 або пізніша версія, щоб отримати новий компілятор. (Linux)
* Підсистема Windows для Linux (WSL) не підтримується, але процес складання GNU / Linux, і виконавчі файли повинні працювати. Спільнота буде вирішувати тільки ті проблеми, які відтворюються у власних системах GNU / Linux.
* Запуск Node.js на x86 Windows повинен працювати, і надаваться виконавчі файли. Проте тести в нашій інфраструктурі працюють тільки на WoW64. Більш того, компіляція в x86 Windows є експериментальною і може перестати працювати.

## Підтримуючі набори інструментів
Залежно від платформи хоста вибір компіляторів може варіюватися.
| Операційна система | Версія компілятора                                           |
| ---------------- | -------------------------------------------------------------- |
| Linux            | GCC >= 8.3                                                     |
| Windows          | Visual Studio >= 2019 with the Windows 10 SDK on a 64-bit host |
| macOS            | Xcode >= 11 (Apple LLVM >= 11)                                 |

## Офіційні бінарні платформи та інструменти
Бінарні файли на https://nodejs.org/download/release/ створюються на:
| Бінарні пакети        | Платформа та набір інструментів                                                                               |
| --------------------- | ------------------------------------------------------------------------------------------------------------- |
| darwin-x64 (and .pkg) | macOS 10.15, Xcode Command Line Tools 11 with -mmacosx-version-min=10.13                                      |
| linux-arm64           | CentOS 7 with devtoolset-8 / GCC 8 <sup>[8](#fn8)</sup>                                                       |
| linux-armv7l          | Cross-compiled on Ubuntu 18.04 x64 with [custom GCC toolchain](https://github.com/rvagg/rpi-newer-crosstools) |
| linux-ppc64le         | CentOS 7 with devtoolset-8 / GCC 8 <sup>[8](#fn8)</sup>                                                       |
| linux-s390x           | RHEL 7 with devtoolset-8 / GCC 8 <sup>[8](#fn8)</sup>                                                         |
| linux-x64             | CentOS 7 with devtoolset-8 / GCC 8 <sup>[8](#fn8)</sup>                                                       |
| win-x64 and win-x86   | Windows 2012 R2 (x64) with Visual Studio 2019                                                                 |

## Основи npm:
Npm (node package manager) - це менеджер пакетів Node.js.
Npm працює, виконуючи одну зі своїх двох ролей:
- Це широко використовуваний репозиторій для публікації проектів Node.js з відкритим вихідним кодом. Це означає, що це онлайн-платформа, де кожен може публікувати та ділитися інструментами, написаними на JavaScript.
- Npm - це інструмент командного рядка, який допомагає взаємодіяти з онлайн-платформами, такими як браузери і сервери. Ця утиліта допомагає в установці і видаленні пакетів, управлінні версіями і залежностями, необхідними для запуску проекту.

## Установка пакетів:
Так як користувачі частіше скачують пакети (16 млрд завантажень проти 13 млн публікацій), добре б розібратися, як їх встановлювати.
- npm install
``` npm install ``` - команда, що встановлює пакети.
npm зробив установку пакетів JavaScript настільки простою, що команда часто використовується некоректно.
При додаванні прапора ```--production``` встановлюються тільки потрібні для роботи програми залежно з dependencies, що не сильно збільшить розмір ```node_modules```.

## Локальна установка пакетів
Для демонстрації візьмемо пакет ```http-server```.
```http-server``` - пакет, який надає більш простий інтерфейс у використанні базового модуля ```http.Server з node.js```. Цей модуль хороший приклад використання API як для бінарного CLI, так і для плагіна ```node.js```.
```npm install http-server```
Так ми встановимо ```http-server``` в нашій робочій директорії.
Ви побачите нову папку в ```node_modules```.

## Глобальна установка пакетів
* Якщо ви хочете щоб пакет був доступний всім додаткам, його потрібно встановити глобально:
```npm install http-server -g```
Прапор ```-g``` означає, що ```http-server``` повинен бути встановлений глобально і бути доступними для всіх додатків.
Тепер ми можемо викликати його require ('http-server') в будь-якому нашому додатку.
Крім того, оскільки http-server пакет має свій виконуваний файл, то цей файл також буде встановлений як виконуваний http-server і доступний в командах.
Тепер ви можете просто запустити команду: ```http-server```.

## Розуміння різниці між глобальної і локальної установкою
За замовчуванням npm буде встановлювати всі пакети в локальному каталозі, в яких ви зараз працюєте. Це правильно. Це може здатися трохи заплутаним, якщо ви раніше працювали з попередніми системами управління пакетами.

## Видалення локально встановленого пакета
```npm uninstall http-server```
## Видалення глобально встановленого пакета
```npm uninstall http-server -g```
## Установка певної версії пакета
```npm install http-server@0.3.0```
## Установка модуля з GitHub
**Важливо.** У деяких випадках будуть патчі, Форк або гілки, які ви хочете використовувати, але які ще не були опубліковані в npm. На щастя вихідні коди для більшості npm модулів також доступна на [github](www.github.com)

## npm ci
Якщо ```npm install --production``` оптимальний для продакшена, чи існує аналогічна команда для локальної розробки? Так, вона називається ```npm ci```.
Як і раніше, якщо ```package-lock.json``` ще не існує в проекті, він буде згенерований при виклику ```npm install.npm ci``` звертається до Lock-файлу для завантаження точної версії пакетів. Таким чином, на різних машинах набір пакетів залишиться незмінним.

## dependencies и devDependencies
```dependencies і devdependencies```представляють собою словники з іменами npm-бібліотек (ключ) і їх семантичні версії (значення). Приклад з шаблону TypeScript Action:  
```{
 "dependencies": {
    "@actions/core": "^1.2.3",
    "@actions/github": "^2.1.1"
  },
  "devDependencies": {
    "@types/jest": "^25.1.4",
    "@types/node": "^13.9.0",
    "@typescript-eslint/parser": "^2.22.0",
    "@zeit/ncc": "^0.21.1",
    "eslint": "^6.8.0",
    "eslint-plugin-github": "^3.4.1",
    "eslint-plugin-jest": "^23.8.2",
    "jest": "^25.1.0",
    "jest-circus": "^25.1.0",
    "js-yaml": "^3.13.1",
    "prettier": "^1.19.1",
    "ts-jest": "^25.2.1",
    "typescript": "^3.8.3"
  }
}
```
Ці залежності встановлюються командної ```npm install``` з прапорами ```--save і --save-dev```. Вони призначені відповідно для використання в продакшені і розробці.

## Про версіонування:
* Останній мінорний реліз. Наприклад, реліз 1.0.4 встановить версію 1.3.0, якщо це останній мінорний реліз в серії 1 мажорного релізу.
* Останній патч-реліз, 1.0.4 встановить 1.0.7, якщо ця остання мінорна версія в серії мінорних релізів 1.0.
Всі версії пакетів будуть відображені в створеному файлі package-lock.json.

## Розміщення пакетів
Перейдемо від споживання пакетів до їх розміщення.
* npm publish
Надіслати пакет в **npmjs.com** дуже просто - потрібно набрати в консолі ```npm publish```. Важлива частина, якої нехтують автори - Версіонування.
- **Мажорна версія: коли зроблені знову/назад несумісні зміни API.**
- **Мінорна версія: коли ви додаєте нову функціональність, не порушуючи зворотної сумісності.**
- **Патч-версія: коли ви робите назад сумісні виправлення.**
Ще більш важливо слідувати вищевказаним правилам при публікації власних пакетів, щоб гарантувати, що ви не порушуєте чиюсь сумісність, так як за замовчуванням в npm береться наступна молодша версія.

## Оновлення пакетів
Для оновлення пакетів служить наступна команда: ```npm update```
Отримавши цю команду, npm перевірить всі пакети на наявність їх нових версій, і, якщо знайде їх нові версії, відповідні обмеженням на версії пакетів, заданим в ```package.json```, встановить їх.

Оновити можна і окремий пакет:
```npm update <package-name>```

## Зміна версії node
Для встановлення певної версії node.js служить наступна команда:
```npm install node@version```

## Файл package.json
Файл ```package.json``` є найважливішим елементом безлічі проектів, заснованих на екосистемі Node.js. ```Package.json``` є чимось на зразок файлу-маніфесту для проекту.
Можна виділити наступні властивості:
* **name - задає ім'я програми (пакета).
* **version - містить відомості про поточну версію програми.
* **description - короткий опис програми.
* **main - задає точку входу в додаток.
* **private - якщо ця властивість встановлено в true, це дозволяє запобігти випадкову публікацію пакета в npm.
* **scripts - задає набір Node.js-скриптів, які можна запускати.
* **dependencies - містить список npm-пакетів, від яких залежить додаток.
* **devDependencies - містить список npm-пакетів, які використовуються при розробці проекту, але не при його реальній роботі.
* **engines - задає список версій Node.js, на яких працює додаток.
* **browserlist - використовується для зберігання списку браузерів (і їх версій), які має підтримувати додаток.

## Детальніше на прикладі ```package.json```
```{
  "name": "project",
  "version": "1.0.0",
  "description": "Test",
  "main": "test.js",
  "license": "ISC",
  "private": true,
  "dependencies": {
    "lodash": "latest"
  },
  "scripts": {
    "start":"node test.js"
  },
  "repository": "github:https://github.com/lodash/lodash"
}
```
## Версії пакетів і семантичне версіонування
Hомери версій пакетів задаються не тільки у вигляді звичайних чисел, розділених точками, але і з використанням деяких спеціальних символів. Наприклад, у вигляді ~ 3.0.0 або ^ 0.13.0. Тут використані так звані специфікатор версій, які визначають діапазон версій пакетів, придатних для використання в нашому пакеті. Такі правила використання специфікаторів версій:
*  ~: Якщо ви задаєте версію у вигляді ~ 0.13.0 це означає, що вас цікавлять лише патч-релізи пакета. Тобто, пакет 0.13.1 вам підійде, а 0.14.0 - немає.
Наприклад: ```npm install lodash@"~4.17.1"```
Результат:
```
package.json
{
  "name": "untitled",
  "version": "1.0.0",
  "dependencies": {
    "lodash": "^4.17.15"
  }
}
```
* ^: Якщо номер версії заданий у вигляді ^ 0.13.0, це означає, що вам підходять нові патч-версії і мінорні версії пакету. Тобто, вас влаштують версії пакету 0.13.1, 0.14.0, і так далі.
Наприклад: ```npm install lodash@"^4.15.0"```
Результат:
```
package.json
{
  "name": "untitled",
  "version": "1.0.0",
  "dependencies": {
    "lodash": "^4.17.15"
  }
}
```
* *: Скориставшись цим символом, ви повідомляєте системі, що вас влаштують будь-які свіжі версії пакету, в тому числі - його нові мажорні релізи.
Наприклад: ```npm install lodash@"*3.10.1"```
Результат:
```
package.json
{
  "name": "untitled",
  "version": "1.0.0",
  "dependencies": {
    "lodash": "^4.17.15"
  }
}
```
* >: Підходять будь-які версії пакету, які більше заданої.
Наприклад: ```npm install lodash@">2.4.2"```
Результат:
```
package.json
{
  "name": "untitled",
  "version": "1.0.0",
  "dependencies": {
    "lodash": "^4.17.15"
  }
}
```
* <: Вас цікавлять пакети, версії яких менше заданої.
Наприклад: ```npm install lodash@"<4.17.15"```
Результат:
```
package.json
{
  "name": "untitled",
  "version": "1.0.0",
  "dependencies": {
    "lodash": "^4.17.14"
  }
}
```
Більшість вищеописаних специфікаторів можна комбінувати, наприклад, задаючи діапазони відповідних версій пакетів-залежностей. Скажімо, конструкція виду 1.0.0 || > = 1.1.0 <1.2.0 вказує на те, що планується використовувати або версію пакета 1.0.0, або версію, номер якої більше або дорівнює 1.1.0, але менше 1.2.0.

* Файл package.json
Файл ```package.json``` содержит в себе информацию о вашем приложении: название, версия, зависимости и тому подобное. Любая директория, в которой есть этот файл, интерпретируется как Node.js-пакет, даже если вы не собираетесь публиковать его.
Способ использования файла ```package.json``` зависит от того, собираетесь ли вы скачивать пакет или публиковать его.

* Завантаження пакетів
Якщо ви хочете скачати пакет вручну, вам необов'язково використовувати для цього ```package.json```. Ви можете виконати в терміналі команду npm з назвою потрібного пакету в якості аргументу команди, і пакет буде автоматично завантажений в поточну директорію. наприклад:
```$ Npm install canvas-chart```
Також для скачування пакетів ви можете використовувати ```package.json```. Створіть в директорії вашого проекту файл ```package.json```, і додайте в нього наступний код (ми не вказуємо назву нашого пакета і версію, так як ми не збираємося його публікувати; ми вказуємо назву і версію пакетів для завантаження):
```
{
  "devDependencies": {
    "canvas-chart": "~1.3.0"
  }
}
```
* Потім збережіть файл і виконайте в терміналі команду ```npm install```.
- Якщо ви хочете використовувати в своєму проекті безліч пакетів, то краще вказати їх ```package.json``` замість того, щоб кожного разу викачувати їх через термінал.
- Якщо ви використовуєте ```package.json``` для скачування пакетів, то виходить, що ви створюєте пакет для скачування пакетів. Я знаю, що це дивно, але це працює.
- Якщо який-небудь пакет має залежності, то npm знайде їх через package.json завантаженні і завантажить їх. У нашому випадку у пакета ```canvas-chart``` теж є файл ```package.json``` з прописаними в ньому залежностями.

* Публікація пакета

Щоб опублікувати пакет, вам буде потрібно зібрати всі вихідні коди і файл package.json в одній директорії. У package.json повинні бути вказані назва, версія і залежності пакета. наприклад:
```
{
  "name": "canvas-project",
  "version": "0.1.0",
  "devDependencies": {
    "canvas-chart": "~1.3.0"
  }
}
```
Подивившись на цей код, ми можемо сказати, що пакет «canvas-project» залежить від пакета «canvas-chart». Опублікувати пакет можна за допомогою комадни ```npm publish```.

* Файл package-lock.json

- Файл ```package-lock.json``` використовується з моменту появи npm версії 5. Він створюється автоматично при установці Node.js-пакетів. Цей файл вирішує вельми специфічну проблему, яка не вирішується засобами ```package.json```. У ```package.json``` можна вказати, які оновлення якогось пакета вам підходять (патч-версії або мінорні версії) з використанням вищеописаних специфікаторів версій.
- У Git НЕ комітять папку node_modules, так як *зазвичай вона має величезні розміри*. Коли ви намагаєтеся відтворити проект на іншому комп'ютері, то використання команди ```npm install``` призведе до того, що, якщо, при використанні специфікатор ~ в застосуванні до версії якогось пакета, вийшов його патч-реліз, встановлений буде не той пакет, який використовувався при розробці, а саме цей патч-реліз. Те ж саме стосується і специфікатор ^. Якщо ж при вказівці версії пакету специфікатор не використовувалися, то буде встановлена саме його зазначена версія і проблема, про яку йде мова, опиниться в такій ситуації неактуальною.
- Файл ```package-lock.json``` зберігає в незмінному вигляді відомості про версії кожного встановленого пакета і *npm* буде використовувати саме ці версії пакетів при виконанні команди npm install. Ця концепція не нова, менеджери пакетів, що застосовуються в інших мовах програмування (менеджера Composer в PHP) використовують схожу систему багато років.
- Файл ```package-lock.json``` потрібно відправити в Git-репозиторій, що дозволить іншим людям завантажити його в тому випадку, якщо проект є загальнодоступним, або тоді, коли його розробкою займається команда програмістів, або якщо ви використовуєте Git для розгортання проекту.
- Версії залежностей будуть оновлені в ```package-lock.json``` після виконання команди ```npm update```. У кожного файл ```package-lock.json``` є поле **version**, є поле **resolved**, яке вказує на розташування пакета, і строкове властивість **integrity**, яке можна використовувати для перевірки цілісності пакету.






