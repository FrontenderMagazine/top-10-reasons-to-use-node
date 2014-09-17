# Топ-10 причин использовать Node.js

Есть множество серьёзных причин использовать Node.js, вне зависимости от вашего уровня квалификации. Предлагаю вам ознакомиться с некоторыми из самых значительных причин использовать и любить Node.

Понимаю. Вы не какой-то рядовой разработчик. Вы не собираетесь использовать крутую модную платформу просто потому, что её используют другие. Потому вы никогда всерьёз не присматривались к [Node.js][1] (или же ваш шеф пока это не одобряет). Что ж, время пересмотреть свою позицию. Существует множество серьёзных, рациональных причин использовать Node. Вот десять из них.

![Node.js][Node.js]

## 1. Вы уже знаете JavaScript

Дайте угадаю. Вы используете полнофункциональный фреймворк на стороне клиента ([Angular][2], [Ember][3], [Backbone][4]) и серверный RESTful API, который гоняет JSON туда и обратно. Даже если вы не используете один из этих фреймворков, вы написали свой на основе jQuery. Следовательно, если вы не используете Node.js на сервере, вы постоянно выполняете преобразования. Преобразовываются две вещи: 1) логика в вашей голове с языка JavaScript на серверный фреймворк и 2) HTTP-данные с JSON в ваши серверные объекты.

Используя JavaScript по всему приложению, вы выигрываете не только в плане сохранения умственных сил, но и в плане практичной полезности. Обеспечивая возможность повторного использования ваших моделей и шаблонов, вы уменьшаете размер своего приложения, что уменьшает его сложность и вероятность возникновения ошибок.

Язык JavaScript завоёвывает мир. В ближайшее время ситуация вряд ли изменится. На каждом компьютере мира есть среда выполнения JavaScript и похоже так будет и дальше.

## 2. Быстрота

Node.js - это среда выполнения JavaScript, в которой используется движок V8, разработанный Google для Chrome. V8 компилирует и выполняет JavaScript на сверхзвуковой скорости в основном благодаря тому, что V8 компилирует JavaScript в родной машинный код.

![сверхзвуковой реактивный самолёт][сверхзвуковой реактивный самолёт]

В добавок к сверхзвуковому выполнению JavaScript, настоящим чудом Node.js является событийный цикл. Событийный цикл - это единый поток, который выполняет все операции ввода-вывода асинхронно. Традиционно, операции ввода-вывода выполняются либо синхронно (блокирующие) либо асинхронно путем порождения параллельных потоков для выполнения работы. Такой старый подход требует большое количество памяти и создаёт общеизвестные сложности при программировании. В отличии от него, когда приложению Node нужно выполнить операцию ввода-вывода, оно посылает асинхронную задачу в событийный цикл вместе с функцией обратного вызова и продолжает выполнять остальную часть программы. После завершения асинхронной операции событийный цикл возвращается к этой задаче, чтобы выполнить функцию обратного вызова.

Другими словами, чтение и запись в сетевых соединениях, чтение/запись в файловых системах и чтение/запись в базе данных - все очень часто встречающиеся задачи в веб-приложениях - в Node выполняются очень, очень быстро. Node позволяет создавать быстрые изменяемые сетевые приложения, способные выдерживать большое количество подключений с высокой производительностью.

## 3. Оснащение

![npm][пакетный менеджер Node.js]

[npm][5] - это пакетный менеджер Node.js и он... просто изумителен. Конечно же, он напоминает пакетные менеджеры из других экосистем, однако пакетный менеджер Node быстр, хорошо продуман и последователен. Он отлично справляется с определением и установкой проектных зависимостей. Он обеспечивает изолированное хранение пакетов каждого проекта, предупреждая конфликты версий. А также выполняет глобальную установку shell-команд и зависимых от платформы бинарных файлов. Не помню чтобы используя пакетный менеджер Node мне приходилось задаваться вопросами «Почему эти модули конфликтуют? Где установлен этот модуль? Почему он выбирает эту версию, а не другую?»

[grunt][6] - достойный почитания таск-менеджер, однако новички в этой сфере, [gulp][7], [brunch][8] и [broccoli][9], уделяют большое внимание сборкам, которые выполняют преобразование файлов и используют преимущество файловых потоков JavaScript.

## 4. Опять же, вы уже знаете JavaScript

![Mongo][Mongo]

Итак, вы решили использовать на сервере JavaScript и гордитесь своим решением, позволяющим избежать преобразования клиентских данных в серверные данные. Однако их сохранение в базе данных требует ещё больших преобразований!

Есть хорошие новости. Если вы используете объектно-ориентированную базу данных вроде [Mongo][10], вы можете вывести JavaScript на уровень персистентности. 

Использование Node.js позволяет использовать один и тот же язык на стороне клиента, на сервере и в базе данных. Вы можете хранить данные в родном JSON-формате повсюду, начиная с браузера и заканчивая диском.

## 5. Простота работы с режимом реального времени

Если Node.js так хорошо справляется с большим количеством параллельных подключений, довольно логично, что он хорошо справляется и с многопользовательскими веб-приложениями, работающими в режиме реального времени, такими как чаты и игры. Событийный цикл Node удовлетворяет потребности нескольких пользователей. Производительность в режиме реального времени достигается за счёт использования протокола WebSocket. Он представляет собой двусторонние каналы передачи данных между клиентом и сервером. Таким образом, сервер может отправлять данные клиенту так же легко, как и клиент серверу. Протокол WebSocket работает через TCP, позволяя избежать лишней нагрузки на HTTP.

[Socket.io][11] - это одна из наиболее популярных библиотек WebSocket, позволяющая сделать разработку коллективных веб-приложений убийственно простой. Вот простой сервер, использующий socket.io:

    var app = require('http').createServer(handler)
    var io = require('socket.io')(app);

    app.listen(8080);

    io.on('connection', function (socket) {
  
      // Отправка сообщения клиенту
      socket.emit('event to client', { hello: 'world' });

      // Обработка сообщения от клиента
      socket.on('event from client, function (data) {
        console.log(data);
      });
    });

## 6. Потоковая передача данных

Традиционно, веб-фреймворки трактуют HTTP-запросы и ответы как цельные объекты данных. По сути, они на самом деле являются потоками ввода-вывода, как вы уже догадались, если вам приходилось иметь дело с потоковой передачей файла из файловой системы. Поскольку Node.js очень хорошо справляется с обработкой операций ввода-вывода, этим можно воспользоваться для создания интересных вещей. Например, можно [перекодировать аудио или видео файлы][12] пока они загружаются, тем самым уменьшая общее время их обработки.

Node может считывать/записывать потоки в WebSocket так же как он может считывать/записывать потоки в HTTP. Например, можно отвести стандартный поток вывода из запущенного процесса на сервере в браузер через WebSocket и отобразить результат на вебстранице в режиме реального времени. 

## 7. Одна кодовая база и режим реального времени в качестве бесплатного бонуса

Если вы добрались так далеко, можете спросить себя: «Если Node.js позволяет мне писать JavaScript код на клиенте и на сервере и упрощает обмен данными между между клиентом и сервером, могу ли я написать веб-приложение, для которого будет использоваться одна кодовая база и в клиенте, и на сервере, с автоматической синхронизацией между ними?»

![Meteor][Meteor]

Ответом на ваш вопрос будет «Да» и для такого приложения будет использоваться фреймворк [Meteor][13]. Meteor - это веб-фреймворк нового поколения, построенный на основе Node. Он использует одну кодовую базу и для клиента, и для сервера. Это позволит вам писать клиентский код, который будет сохраняться прямиком в базе данных. Затем эти данные автоматически сохраняются на сервере. В обратную сторону это работает так же! Любые изменения данных на сервере автоматически отсылаются в клиент. Дальше ещё лучше. Любая вебстраница, на которой отображаются эти данные, реагирует автоматически и обновляется самостоятельно!

    // Сохраняем значение 'name' при щелчке по 'submit' прямо в браузере!
    '.click .submit': function(e, tpl) {
      Users.update(
        { _id: this._id },
        { $set: { name: $('.name').val() }}
      );
    }

## 8. Коллективное администрирование

Каждому проекту с открытым кодом присущ риск того, что он будет заброшен эксплуатационным персоналом, состоящим из добровольцев. Node.js это не грозит. На данный момент он спонсируется компанией [Joyent][14], которая наняла руководителя проекта и других штатных сотрудников, так что за проектом стоит реальная компания, гарантирующая его будущее. Стоит ли упоминать о том большом числе солидных компаний, которые поддерживают его на разных уровнях, в том числе Walmart, Microsoft, Yahoo, Paypal, Voxer и другие.

## 9. Хостинг

![Modulus][Modulus]

Наряду с быстрым введением в обращение, хостинг Node.js на мировом уровне также переживает расцвет. Так, в частности, провайдеры сервиса «платформа как услуга» (*англ. Platform-as-a-Service, PaaS*) такие как [Modulus][15] и другие сокращают алгоритм его развертывания к одной команде. Даже дедушка PaaS, Heroku, уже официально поддерживает развёртывание Node.

## 10. Каждый разработчик знаёт JavaScript (хотя бы чуть-чуть)

Эта часть - для вашего шефа.

С самой зари интернета существуют JavaScript-действия `onclick` и`onmouseover`. Каждому разработчику приходилось писать хотя бы немного JavaScript-кода, даже если этот код сводился к взлому плагина jQuery. Найти талант в мире веб-разработки в наши дни очень трудно. Поэтому когда выбираете веб-платформу, почему бы не выбрать ту, язык которой известен каждому веб-разработчику в мире?

## В завершение, бонус!

Постойте, это ещё не всё! Как и в случае с любой платформой или продуктом, будь они с открытым кодом или нет, сообщество является очень влиятельным фактором. А сообщество, большее чем у Node, нужно ещё поискать. Начиная собраниями и заканчивая конференциями, над этой экосистемой каждый день трудятся действительно умные люди. В то же время, сообщество открыто для всех. Эти умные люди всегда готовы предложить помощью новичкам в Node или же в программировании вообще. Вам не будет неловко за заданный вопрос в IRC-чате или на Github. Сообщество также очень активно, в пакетном менеджере уже насчитывается более 91,000 модулей. И ещё, сообщество не скупится на финансовую поддержку. В 2013 году [было собрано более $70,000 пожертвований][16] от отдельных личностей для оплаты работы общественных серверов npm.

Да, Node сейчас является последним писком моды. Мир веб-разработки непредсказуем, так что на следующей неделе Node вполне может кануть в небытие и появится новый объект всеобщего внимания (возможно им станет Go или Elixir?). Однако попробовать его вам всё же стоит.

[1]: http://nodejs.org/
[2]: https://angularjs.org/
[3]: http://emberjs.com/
[4]: http://backbonejs.org/
[5]: https://www.npmjs.org/
[6]: http://gruntjs.com/
[7]: http://gulpjs.com/
[8]: http://brunch.io/
[9]: https://github.com/broccolijs/broccoli
[10]: http://www.mongodb.org/
[11]: http://socket.io/
[12]: http://transloadit.com/blog/2010/12/realtime-encoding-over-150x-faster/
[13]: https://www.meteor.com/
[14]: https://www.joyent.com/
[15]: https://modulus.io/
[16]: https://scalenpm.nodejitsu.com/

[Node.js]: img/e939.png
[сверхзвуковой реактивный самолёт]: img/3236.jpg
[пакетный менеджер Node.js]: img/2876.png
[Mongo]: img/c02f.png
[Meteor]: img/3004.png
[Modulus]: img/d12b.png