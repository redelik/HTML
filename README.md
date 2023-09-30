# Словарик по HTML
## Скелет сайта:
![Cкелет сайта:](http://u4ilka.kcbux.ru/image/glav-001.jpg)


`<!DOCTYPE html> <!-- Объявление формата документа -->`

`<html>`

`<head> <!-- Техническая информация о документе -->`

`<meta charset="UTF-8"> <!-- Определяем кодировку символов документа -->`

`<title>...</title> <!-- Задаем заголовок документа -->`

`<link rel="stylesheet" type="text/css" href="style.css"> <!-- Подключаем внешнюю таблицу стилей -->`

`<script src="script.js"></script> <!-- Подключаем сценарии -->`

`</head>`

`<body> <!-- Основная часть документа -->`

`</body>`

`</html>`


### Элементы:

1. `<html></html>` - Все, что находится за пределами элемента, не воспринимается браузером как HTML-код и никак им не обрабатывается.

Атрибут manifest: 

С помощью значения атрибута указывается путь к документу кэша манифеста, например:

`<html manifest="about_company.appcache">`

2. `<head></head>` - Раздел содержит техническую информацию о странице: заголовок, описание, ключевые слова для поисковых машин, кодировку и т.д. Введенная в нем информация не отображается в окне браузера, однако содержит данные, которые указывают браузеру, как следует обрабатывать страницу.

3. `<title></title>` - Текст, размещенный внутри элемента <title>, отображается в строке заголовка веб-браузера. Длина заголовка должна быть не более 60 символов, чтобы полностью поместиться в заголовке. Текст заголовка должен содержать максимально полное описание содержимого веб-страницы.

4. `<meta>` - Необязательным элементом раздела <head> является элемент <meta>. С его помощью можно задать описание содержимого страницы и ключевые слова для поисковых машин, автора HTML-документа и прочие свойства метаданных. Элемент <head> может содержать несколько элементов <meta>, потому что в зависимости от используемых атрибутов они несут различную информацию.

`<meta name="description" content="Описание содержимого страницы">`

`<meta name="keywords" content="Ключевые слова через запятую">`

`charset` -	Указывает кодировку символов для текущего HTML-документа: `<meta charset="UTF-8">`

`content` - Содержит произвольный текст, который определяет значение, ассоциируемое с атрибутом `http-equiv` или `name`, в зависимости от их значения.

`http-equiv` - Контролирует действия браузера на данной веб-странице (эквивалент HTTP заголовков). При отображении страницы браузер будет следовать инструкциям, заданным в атрибуте:
`default-style` указывает предпочтительный стиль для использования на странице. Атрибут content должен содержать идентификатор элемента `<link>`, который ссылается на таблицу стилей CSS, или идентификатор элемента `<style>`, содержащего таблицу стилей.

`<refresh>` - указывает время в секундах до перезагрузки страницы или время до перенаправления на другую страницу, если в атрибуте content после указания времени идет строка `"url=адрес_страницы"`.
Автоматическая перезагрузка страницы через заданный промежуток времени, в данном примере, через 30 секунд:
`<meta http-equiv="refresh" content="30">`
Если необходимо сразу перебросить посетителя на другую страницу, то можно указать URL-адрес в параметре `url`:
`<meta http-equiv="refresh" content="0; url=http://mail.ru/">`

`name` - 	Ассоциируется со значением, содержащемся в атрибуте `content`. Не должен использоваться в случае, если для элемента уже заданы атрибуты `http-equiv`, `charset` или `itemprop`.

`cation-name` - указывает название веб-приложения, используемого на странице.

`author` - указывает имя автора документа в свободном формате.

`description` - определяет краткое описание к содержимому страницы, например:
`<meta name="description" content="Описание содержимого страницы">`

`generator` - указывает один из пакетов программного обеспечения, используемого для создания документа, например:
`<meta name="generator" content="WordPress 4.0">`

`keywords` - содержит список ключевых слов, разделенных запятыми, соответствующих содержимому страницы, например:
`<meta name="keywords" content="Ключевые слова через запятую">`
Также атрибут name может принимать следующие значения из расширенной спецификации, такие как `creator`, `googlebot`, `publisher`, `robots`, `slurp`, `viewport`, хотя ни одно из них еще не было официально принято.


5. `<body></body>` - В разделе <body> располагается все содержимое документа. Для элемента доступны атрибуты:

`onafterprint` - Событие, срабатывающее после отправки страницы на печать или после закрытия окна печати.

`onbeforeprint` - Событие, срабатывающее перед отправкой страницы на печать.

`onbeforeunload` - Событие срабатывает, когда посетитель инициировал переход на другую страницу или нажал «закрыть окно». Позволяет отображать сообщение в диалоговом окне подтверждения, чтобы сообщить пользователю, хочет ли он остаться или покинуть текущую страницу.

`onhashchange` - Событие срабатывает, когда меняется hash-часть URL, например, когда пользователь перейдет с адреса example.domain/test.aspx#page1 на example.domain/test.aspx#page2.

`onmessage` - Событие происходит, когда сообщение получено через источник события.

`onoffline` - Событие вызывается браузером в том случае, когда браузер определит, что соединение с интернет пропало.

`ononline` - Событие вызывается браузером в том случае, когда соединение с интернет возобновилось.

`onpagehide` - Событие происходит, когда пользователь покидает страницу посредством навигации, например, нажав на ссылку, обновив страницу, заполнив форму и т.д.

`onpageshow` - Событие происходит, когда пользователь переходит на веб-страницу, после события onload.

`onunload` - Событие срабатывает если страница не загрузилась по каким-либо причинам, либо при закрытии окна браузера.
