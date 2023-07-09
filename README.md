# Модуль NSPanel

![image](https://docs.nspanel.pky.eu/img/nspanel-rl.png)

Данный модуль позволяет подключать панели NSPanel в систему [MajorDoMo](https://github.com/sergejey/majordomo).

Панель представляет собой сенсорный экран с двумя физическими кнопками.
Панель может быть установлена в обычный подрозетник (обязательно наличие фазы и ноля!).
Физические кнопки управляют двумя встроенными реле, но могут быть переназначены на другие действия.
Обмен данными с сервером осуществляется по WiFi и протоколу MQTT.

**Внимание:** Модуль основан на проекте [NsPanel Lovelace UI](https://docs.nspanel.pky.eu/). Для работы модуля необходимо, чтобы панель была перепрошита
на платформу Tasmota и установлено дополнительное ПО для экрана.
Для прошивки панели понадобится USB-TTL адаптер и провода для подключения (паять не нужно!).
Подробную инструкцию по установке прошивки можно найти [здесь](https://docs.nspanel.pky.eu/prepare_nspanel_ioBroker/) (англ.)

После подготовки панели, её настройка сводится к подключению к MQTT-серверу.
К этому же серверу должен быть подключен модуль, также в настройках модуля должен быть
прописан базовый топик, куда будут приходить данные всех панелей.

Функционал модуля на очень раннем этапе разработке и возможны сбои в работе, о которых
вы можете сообщать автору.

На данный момент поддерживается ряд базовых возможностей:

- Экран типа список элементов
- Экран типа набор иконок
- Экран типа QR-код
- Хранитель экрана
- Приём уведомлений на панель

Поддерживаемые типы элементов (для списка и иконок):
- Переключатель On/Off
- Кнопка (для запуска методов/сценариев)
- Текст (для показаний датчиков)

Для каждого элемента можно настроить поведение (связанный объект/свойство/метод),
иконку ([список](https://docs.nspanel.pky.eu/icon-cheatsheet.html)), цвет.

Настройка интерфейса и поведения панели осуществляется через редактирование JSON-конфигурации
(есть возможность поставить демо-конфигурацию).

Планы по развитию:
- Более удобный интерфейс работы с конфигурацией панели
- Расширенная настройка хранителя экрана (вывод статусов/датчиков)
- Поддержка новых типов карточек:
  - Карточка для настройки освещения (яркость, температура, цвет)
  - Термостат    
  - Сигнализация  
  - Медиа-плеер
  - Будильник/таймер
- Поддержка новых типов элементов
  - Позиционируемый регулятор (для установки уровня)

Обсуждение функционала в телеграм-канале [MajorDoMo](https://t.me/MajorDoMoRu)

