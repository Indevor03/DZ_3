# Инструкция работы в Markdown

## Синтаксис в Markdown

Команды, используемы в Markdown

add - Добавление файлов в индекс git.

branch - работа с втеками: просмотр, создание, удаление.

checkout - переход на разные ветки репозитория и восстанавление файлов в рабочем бранче (приводит содержимое в соответствие с удаленным репозиторием)

clear - удаление файлов, которые не отслеживаются в репозитории (файлы которые попали в папку, но не были добавлены в индекс с помощью команды git add)

clone - клонирование репозиторий

commit - добавление описания к файлам, которые ранее были добавлены в индекс с помощью команды git add.

diff - сравнение содержимого (фиксами, деревьями и так далее)

init - инициализация нового репозитория или повторная инициализация существующего.

log - журнал коммитов

merge - объединение веток

pull - скачивание файлов из другого репозитория

push - отправка на сервер файлов, которые были добавлены в индекс с помощью команды git add

reset - сброс состояния изменений для текущей ветки. Позволяет без объединений заменить файлы при выполнении git pull

## Работа с текстом

Курсив - обрамление текста звёздочками (*). Пример:

*Текст*

Полужирный текст - обрамление текста двумя звёздочками (**). Пример:

**Текст**

Заголовок - решётка (#) перед названием:
# Текст

Подзаголовок - две решётки (##) перед текстом. Пример:
## Текст

Альтернативное выделение текста знаком нижнего подчёркивания для одновременного использования двух способов. Пример:

_Текст может выглядть *так* или **так**_

## Работа со списками

*Ненумерованный список - звёздочка пробел текст* Пример:
* Элемент 1
* элемент 2

*Нумерованный список - цыфра точка пробел текст.* Пример:
1. Элемент 1
2. Элемент 2

## Работа с изображениями

*Для ввода изображения ввести команду: ! [] (). где ! - команда для ввода изображения, [] - текст к изображению, если оно не появиться, () - файл изображения. Пример:*

![CCCР](sssr-flag-gerb.jpg)

*Для вставки изображения ввести команду: ! [] (), где ! -это команда для вставки изображения, [] - отображение текста в случае отсутствия изображения, () - файл изображения. Пример:*


![CCCР](sssr-flag-gerb.jpg)

![ВЛКСМ](VLKSM.jpg)

## Работа с ссылками

**Markdown поддерживает два стиля оформления ссылок:**

* _**Гиперссылка, с немедленным указанием адреса (внутритекстовая)**_

* _**Гиперссылка, подобная сноске**_

*Подразумевается, что помимо URL-адреса существует еще текст ссылки. Он заключается в квадратные скобки. Для создания внутритекстовой гиперссылки необходимо использовать круглые скобки сразу после закрывающей квадратной. Внутри них необходимо поместить URL-адрес. Там же располагается название, заключенное в кавычки, которое будет отображаться при наведении, но этот пункт не является обязательным.*

  [пример](http://yandex.ru"Необязательная подсказка")

*В результате на экран выводится следующее: пример При ссылке на локальную директорию возможно использование относительного пути (от текущей страницы, сайта и т.п.)*

*При создании сносной гиперссылки вместо целевого адреса используется вторая пара квадратных скобок, внутри которых помещается метка, идентификатор ссылки (id)*.

[пример][id](http://yandex.ru)

*Также, можно использовать пробел, чтобы отделять 2 пары квадратных скобок:*

[пример] [id]:

*В этом случае возможно определить идентификатор в любом месте документа:*

[id]:http://yandex.ru 

В результате на экран выводится следующее: 
пример

[id][id]: http://yandex.ru

"Необязательная подсказка" - иными словами, она состоит из следующих элементов:

* *Идентификатор ссылки, окружённый квадратными скобками (которым может предшествовать необязательный отступ от одного до трёх пробелов)*

* *Двоеточие*

* *Один или несколько пробелов (или символов табуляции)*

* *URL гиперссылки*

* *Необязательный заголовок (подсказка к изображению, которая всплывает при наведении на него) гиперссылки, заключённый либо в двойные или одиночные кавычки, либо в скобки*

*Идентификаторы ссылок могут состоять из букв, цифр, пробелов и знаков пунктуации, однако они не чувствительны к регистру. То есть эти два варианта эквивалентны:*

[текст ссылки][a]
[текст ссылки][A]

*в Markdown позволяет также использовать неявно выраженный идентификатор (сокращенный). В этом случае метка не приводится, вместо неё текст гиперссылки используется и в качестве её имени, а вторая пара квадратных скобок остаётся пустою. Например, чтобы сделать слово «yandex» гиперссылкой, ведущей на сайт http://yandex.ru, достаточно написать: [yandex][] и затем определить гиперссылку:*

[yandex]:(http://yandex.ru)

*В результате на экран выводится следующее:*

[yandex][yandex]: http://yandex.ru



*Автоматическая ссылка на адрес электронной почты в Markdown выглядит следующим образом (без пробелов послетреугольных скобок)*
*< address@example.com >*
*В результате на экран выводится следующее:*

address@mail.ru

## Работа с таблицами

## Работа с цитатами

*Для создания цитат в языке Markdown используется знак «больше» («>»), а также есть возможно создавать вложенные цитаты - цитаты внутри цитат. Для их разметки используются дополнительные уровни знаков цитирования («>»). Цитаты в Markdown могут содержать всевозможные элементы разметки. Цитаты в языке Markdown выглядят следующим образом:*

>Это пример цитат
>>И подзаголовоков цитат
>>>Нескольких уровней (цитата в цитате)

*Уровень цитирования не может превышать 15-ти*

## Работа с ветками

*Создание веток используется для редактирвания конечного проекта, не затрагивая первначальный вариант, в виде черновика*

### Создание

*Для создания веток используется команда branch.* Пример:

**git branch <имя ветки>**.

*Для перехода из однй ветки в другую используется команда:*

**git checkout <имя ветки>**

### Слияние

*После корректировки изменений в ветке, для переноса изменённой информации в итоговый проект (оснвную ветку) оспользуется команда:*

**git merge <имя ветки>**

*в которой производилась корректировка. Примечание: перенос из одной ветки в другую осуществляется из той, в которую нужно добавить изменения.*

### Конфликты

*Возникновение конфликтов появляется при задвоении информации в ветках. Для разрешения конфликтов необходимо самостоятельно (в ручную) выбрать нужный вариант: входящий, настоящий или оба варианта.*

### Визуализация

*Для отображения веток необходимо использовать команду:

**git log -graph**.

*В окне терминала отобразиться информация о всех созданных ветках и имзенениях в них. Таким образом, появляется возможность контроля внесённых изменений в ветках и их сравнении.*

### Удаление

*После внесённых всех изменений в "черновой" ветке и переноса в основной проект (слияния веток), ненужную ветку можно удалить при помощи команды:

**git branch -d <имя ветки>**.

*Рекомендуется использовать флаг -d (прописная "d"), так как при использовании заглавной "D" есть вероятность удаления всех внесённых изменений.*

## Работа с удалёнными репозиториями в Git и GitHub

1. Создать аккаунт на GitHub.com
2. Создать локальный репозиторий
3. Синхронизировать локальный и удалённый репозитории.

 GitHub при создании нового репозитория подскажет, как это можно сделать.

4. авторизоваться на удалённом репозитории (в случае первого создания репозитория)
5. Извлечь (pull) файл из удалённого репозитория в локальный репозиторий на личном компютере. Проверить изменения “с другого компьютера”
6. Отправить (push) свой изменённый локальный репозиторий в удалённый (на GitHub), при этом, возможно, вам необходимо будет авторизоваться; если нет аккаунта - создать новый.

## Заключение

Git - программа для создания файлов репозиториев, их изменений и сохранений.

GitHub - сервис для хранения репозиториев в интернете, осуществеления доступа к ним и обеспечения возможности корректировки (внесений исправлений) другими лицами.