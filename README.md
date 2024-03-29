# AzureIoTCenter1CMonitor
Мониторинг 1С с использованием Azure Iot Center

## Ability.Monitor
Решение Ability.Monitor обеспечивает бизнес стабильно-работающей системой 1С, а ИТ службу удобным инструментом для контроля основных жизненно важных параметров функционирования системы 1С.

Конструктивно сервис строится на аналитике событий, которые формирует 1С и системы, на которых 1С базируется.

<img src="https://github.com/ability-group/AzureIoTCenter1CMonitor/blob/master/images/AzureIoTCenter1CMonitor-Home.png" width=500px>

Ability.Monitor позволяет отображать аналитическую информацию на заранее настроенных дашбордах, в удобном для специалистов виде.

Решение включает в себя 
* Сервис сбора статистики с серверов, входящих в инфраструктуру, подерживающих работу систем 1С
* Решение на платформеAzure IoT Center для сбора, аналитики и мониторинга телеметрии, получаемой с зарегистрированных серверов.

Сбор телеметрии осуществляется с использованием платформы IoT Central. В панели мониторинга зарегистрированы сервера для мониторинга

<img src="https://github.com/ability-group/AzureIoTCenter1CMonitor/blob/master/images/AzureIoTCenter1CMonitor-Dashboard.png" width=500px>

## Архитектура решения

<img src="https://github.com/ability-group/AzureIoTCenter1CMonitor/blob/master/images/AzureIoTCenter1CMonitor-Scheme.png" width=500px>

## Сбор телеметрии с серверов
<img src="https://github.com/ability-group/AzureIoTCenter1CMonitor/blob/master/images/AzureIoTCenter1CMonitor-Service.png" width=500px>

Служба мониторинга "Абилити Монитор" отправляет телеметрию и характеристики сервера в IoT Central используя MQTT-транспорт.

Передаются характеристики:
* Название организации
* Название сервера
* Местоположение сервера


Состав измерений определяется конфигурационной настройкой. Базовый состав параметров для мониторинга производительности:

| Объект  | Счетчик  | Описание  |
|---|---|---|
| Память  | Memory \ Pages/sec  | Характеризует интенсивность обмена между дисковой подсистемой и оперативной памятью. Обращение к дисковой системе происходит из-за того, что запрашиваемые страницы отсутствуют в оперативной памяти.  |
| Процессор  | Processor \ %Processor Time  | Время, которое процессор тратит на выполнение полезной работы, в процентах от общего системного времени.  |
| Процессор  | System \ Processor Queue Length  | Длина очереди к процессору.  |
| Дисковая подсистема  | Physical Disk \ %Disk Time  | Процент времени, которое диск был занят, обслуживая запросы чтения или записи.  |
| Дисковая подсистема  | Physical Disk \ Avg. Disk Queue Length  | Показывает эффективность работы дисковой подсистемы. Представляет собой среднюю длину очереди запросов к диску.  |
| Сетевой интерфейс  | Network Interface \ Bytes Total/sec  | Скорость, с которой происходит получение или посылка байт через сетевой интерфейс  |
| Блокировки  | SQL Server: Locks \ Lock Wait Time (ms)  | Показывает общее время ожидания (в миллисекундах) выполнения запросов на блокировку за последнюю секунду  |
| Блокировки  | SQL Server: Locks \ Average Wait Time (ms)  | Показывает среднее время ожидания (в миллисекундах) выполнения каждого запроса на блокировку  |
| Блокировки  | SQL Server: Locks \ Number of Deadlocks/sec  | Показывает количество запросов на блокировку в секунду, которые закончились взаимной блокировкой  |




