# Переведенная на русский язык версия плагина Store

Ссылка на оригинал - https://github.com/Kxnrl/Store <br>

Быстрый переход:
<ul>
<li><a href ="https://github.com/segas-segason/store_master_ru#%D0%BE%D1%81%D0%BE%D0%B1%D0%B5%D0%BD%D0%BD%D0%BE%D1%81%D1%82%D0%B8">Особенности</a></li>
<li><a href ="https://github.com/segas-segason/store_master_ru#%D0%BA%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4%D1%8B">Команды</a></li>
<li><a href ="https://github.com/segas-segason/store_master_ru#%D1%83%D1%81%D1%82%D0%B0%D0%BD%D0%BE%D0%B2%D0%BA%D0%B0-%D0%B8-%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0">Установка и настройка</a></li>
<li><a href ="https://github.com/segas-segason/store_master_ru#%D0%B4%D0%BB%D1%8F-%D1%80%D0%B0%D0%B7%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D1%87%D0%B8%D0%BA%D0%BE%D0%B2">Для разработчиков</a></li>
</ul>

<h2>Особенности:</h2>

<h2>Команды:</h2>
<blockquote>sm_ (консоль) = ! (чат)</blockquote>
<ul>
<li><b>sm_store, sm_shop</b> - Открыть меню магазина.</li>
<li><b>sm_inv, sm_inventory</b> - Открыть инвентарь.</li>

<li><b>sm_credits</b> - Показать количество кредитов всем игром на сервере.</li>

<li><b>sm_hide, sm_hideneon, sm_hidetrail</b> - Отключить видимость шапок, питомцев, трейлов и неона, также положительно влияет на FPS.</li>

<li><b>sm_tp</b> - Включитьрежим третьего лица.</li>

<li><b>sm_seeme</b> - Осмотреть внешность персонажа.</li>

<li><b>sm_arms</b> - (administator command) Fix player's arms.</li>
<li><b>sm_cheer</b> - Trigger -> server play sound.</li>
<li><b>sm_crpb</b> - Toggle -> block cheer sound.</li>
<li><b>spray</b> - Trigger -> spary paint.</li>
</ul>

<h2>Установка и настройка:</h2>

1. <a href ="https://build.kxnrl.com/Store/">Скачайте</a> последний билд плагина для своей версии sourcemod (1.9 или 1.10);

2. Распакуйте архив и загрузите на свой сервер:
<ul>
<li>addons</li>
<li>models</li>
<li>materials</li>
<li>particles</li>
<li>sound</li>
</ul>

3. Переименуйте в папке <b>addons/sourcemod/plugins</b> файл store_(GameMode).smx в store.smx (в соответствии с вашим игровым модом):
<ul>
<li></li>
<li></li>
<li></li>
<li></li>
<li></li>
</ul>

4. Импортируйте SQL: <b>addons/sourcemod/configs/database.sql</b>
<blockquote>Если появилась ошибка <code>#1071 - Specified key was too long; max key length is 767 bytes</code>, то найдите строку <code>`unique_id` varchar(192) NOT NULL DEFAULT ''</code> и замените на <code>`unique_id` varchar(191) NOT NULL DEFAULT ''</code></blockquote>

5. Настройте файл: <b>addons/sourcemod/configs/database.cfg</b>, добавив следующий код:
<pre>
<code>
"csgo"
{
    "driver"    "mysql" // не менять
    "host"      "HOSTNAME" // адрес вашего хоста
    "database"  "DATABASE" // название бд
    "user"      "USERNAME" // имя пользователя
    "pass"      "PASSWORD" // пароль
    "port"      "3306"
}
</code>
</pre>

6. Настройте файл: <b>addons/sourcemod/configs/store/items.txt</b>
<pre>
<code>
Код
</code>
</pre>

7. Добавьте в таблицу <b>store_item_parent</b> вашей БД элементы меню из <b>items.txt</b>:

<pre>
<code>
Код
</code>
</pre>

8. Добавьте в таблицу <b>store_item_child</b> вашей БД товары из <b>items.txt</b>:

<pre>
<code>
Код
</code>
</pre>

<h2>Для разработчиков:</h2>
