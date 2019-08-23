UplinkOS_Rus 0.2.20
==========
Готовность локализации ~30%
----------


### Что уже переведено:
1. Заменен основной шрифт.
1. Главное меню.
1. Настройки.
1. Интро нового пользователя.
1. Начальный интерфейс (HUD).
1. Туториал.
1. Ссылки в InterNIC.
1. Не уникальные новости о взломах корпораций.
1. Новости о взломе Сoциальной БД.
1. Новости о взломе Академической БД.
1. Новости о взломе Криминальной БД.
1. Новости о взломе систем с разрушением сервера.
1. Новости о взломе с большим объемом данных.
1. Новости об арестах.
1. 5 уникальных новостей.
1. 12 уникальных писем.
1. Описания программ в магазине.
1. Описания железа в магазине.
1. Описания шлюзов в магазине.
1. Перевод консоли (~50%).
1. Задания ур. 1-5.
1. Письма для соответствующих заданий.
1. Окно чата с заказчиком.
1. Логи.
1. Государственные базы данных.
1. Разделы справки.

### Что не будет переведено:
1. Голоса для голосового анализатора - у меня пока нет возможности качественно записать звук.
2. Многие короткие слова *(см. сложности перевода)*.
3. Названия корпораций и имена людей *(т.к. станет невозможным поиск по базам, см. пункт 4)*.
4. Возможность печатать на русской раскладке (если знаете как это исправить, пожалуйста, свяжитесь со мной).
5. Всё, что не захочет переводить мой левый мизинец задней ноги. Возможно мне в очередной раз надоест и я заброшу проект в третий раз.

### О переводе
За локализацию я взялся т.к. в детстве играл в оригинальную игру в пиратском переводе под названием **"Сеть"**, но из за ошибок перевода она была непроходима. 
Модификация графики **"[Uplink OS](https://www.moddb.com/mods/uplink-os)"** получилась шикарной, рекомендую всем фанатам оригинальной игры ознакомиться с ней. Очень жаль, что *[Cpt.McBacon](https://www.moddb.com/members/cptmcbacon)* и *[JesseTG](https://www.moddb.com/members/jessetg)* прекратили разработку на версии GOLD. Насколько я могу судить, она местами сыровата. Кроме того, авторы модификации собирались сделать возможность простой локализации через XML файлы, но забросили реализацию этой фичи на полпути. В результате мы имеем часть строк жестко закодированных в EXE, а часть - в XML ресурсах игры. 

### Инструментарий
Я пытался связаться с командой разработчиков **"Uplink OS"** для помощи им в разработке и локализации стандартными средствами, но тщетно. Они не отвечают и больше не занимаются проектом. В связи с этим было принято решение локализовать **"UplinkOS"**, но доступными мне средствами. Итак, чем я пользуюсь:

* **Radialix 2/3** - используется для перевода жестко закодированных *ASCII* строк в файле *UplinkOS.exe*
* **IDA** - дизассемблер с которым работает *Radialix* для поиска ссылок на жестко закодированные строки
* **Notepad++** - для перевода части строк вынесенных в XML файлы 
* **Translate my UTF8-HEX** - созданный мной скрипт для удобного перевода UTF8 строк *(см. сложности перевода)*
* **Google/Яндекс переводчик** - в ручном режиме.

#### Сложности перевода
Перевод через программу *Radialix* это фактически более удобная форма редактирования исполняемого файла в HEX-редакторе, где нельзя выходить за рамки отведенного каждой строке места внутри файла. Т.к. при программировании авторы модификации использовали кодировку UTF8 (в ней кириллические символы занимают в 2 раза больше байт чем латинские), то все переводимые жестко закодированные строки приходится сжимать в 2 раза. Чтобы хоть как-то нивелировать этот эффект, мной был написан скрипт *Translate my UTF8-HEX*, который автоматически подставляет вместо кириллических букв похожие латинские (А/A, и/u, ь/b, и тд.), а также подсказывает, на сколько байт следует сократить перевод чтобы он влез в отведенное для строки место. 

Именно по этой причине я не перевожу многие короткие слова (обычно и без перевода понятные). Например слово **No** занимает всего 2 байта, а слово **Нет** уже все 6 байт (4 при замене букв на латинские). У меня была идея заменить **Yes** и **No** на **+** и **-**, но остается десяток других надписей на кнопках, которые перевести уже сложнее, поэтому было решено оставить их как есть. 

### Лицензия
##### Лицензия перевода
Этот перевод является свободным программным обеспечением. Вы можете распространять и/или модифицировать его с сохранением указания автора проекта (**Сергей _"kesha4"_ Макаров**). Не рекомендуется использовать данный перевод и его производные для получения денежной выгоды. 
Этот перевод распространяется в надежде, что он будет полезен, но БЕЗ ВСЯКИХ ГАРАНТИЙ, в том числе подразумеваемых гарантий ТОВАРНОГО СОСТОЯНИЯ ПРИ ПРОДАЖЕ и ГОДНОСТИ ДЛЯ ОПРЕДЕЛЁННОГО ПРИМЕНЕНИЯ. Автор не несет никакой ответственности в случае неполадок вызванных данным продуктом, а также в случае возникновения острого психоза на фоне неточности перевода.
##### Лицензия Uplink
Данный репозиторий содержит оригинальные файлы игры [**Uplink: Hacker Elite** с сайта _GOG.com_](https://www.gog.com/game/uplink_hacker_elite), которые приложены для примера. Удалите их, если вы не покупали игру на указанном сайте. Оригинальные файлы игры содержатся в самом первом коммите. Все права принадлежат разработчику **Introversion Software**. Подробнее см. файл *readme.txt*.
##### Лицензия UplinkOS
Данный репозиторий содержит также оригинальные файлы модификации **[Uplink OS](https://www.moddb.com/mods/uplink-os)** за авторством **[Cpt.McBacon](https://www.moddb.com/members/cptmcbacon)** и **[JesseTG](https://www.moddb.com/members/jessetg)**, все права принадлежат им. Оригинальные файлы модификации содержатся во втором коммите. Подробнее см. файл *UplinkOS_ReadMe.txt*. 

### Контакты

- [Мой E-mail: kesha4elovek@gmail.com](mailto:kesha4elovek@gmail.com)
- [Мой Telegram: @kesha4e](https://t.me/kesha4e)
- [Мой Вконтакте: id209151094](https://vk.com/id209151094)

### Ссылки связанные с проектом:
- [Uplink: Hacker Elite –  GOG.com](https://www.gog.com/game/uplink_hacker_elite)
- [Uplink OS modification (GOLD GOG version)](https://www.moddb.com/mods/uplink-os)
- [Uplink  – Wikipedia](https://ru.wikipedia.org/wiki/Uplink)
