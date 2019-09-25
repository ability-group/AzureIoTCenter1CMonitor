# AzureIoTCenter1CMonitor
Мониторинг 1С с использованием Azure Iot Center

## Ability.Monitor
Решение Ability.Monitor обеспечивает бизнес стабильно-работающей системой 1С, а ИТ службу удобным инструментом для контроля основных жизненно важных параметров функционирования системы 1С.

Конструктивно сервис строится на аналитике событий, которые формирует 1С и системы, на которых 1С базируется.

Ability.Monitor позволяет отображать аналитическую информацию на заранее настроенных дашбордах, в удобном для специалистов виде.

Решение включает в себя 
* Сервис сбора статистики с серверов, входящих в инфраструктуру, подерживающих работу систем 1С
* Решение на платформеAzure IoT Center для сбора, аналитики и мониторинга телеметрии, получаемой с зарегистрированных серверов.

## Архитектура решения

<img src="https://github.com/ability-group/AzureIoTCenter1CMonitor/blob/master/images/AzureIoTCenter1CMonitor-Scheme.png">

## Сбор телметрии с серверов
<img src="https://github.com/ability-group/AzureIoTCenter1CMonitor/blob/master/images/AzureIoTCenter1CMonitor-Service.png">

| Объект  | Счетчик  |   |   |   |
|---|---|---|---|---|
| Память  | Memory \ Pages/sec  |   |   |   |
| Процессор  | Processor \ %Processor Time  |   |   |   |
| Процессор  | System \ Processor Queue Length  |   |   |   |
| Дисковая подсистема  | Physical Disk \ %Disk Time  |   |   |   |
| Дисковая подсистема  | Physical Disk \ Avg. Disk Queue Length  |   |   |   |
| Сетевой интерфейс  | Network Interface \ Bytes Total/sec  |   |   |   |
| Блокировки  | SQL Server: Locks \ Lock Wait Time (ms)  |   |   |   |
| Блокировки  | SQL Server: Locks \ Average Wait Time (ms)  |   |   |   |
| Блокировки  | SQL Server: Locks \ Number of Deadlocks/sec  |   |   |   |

<img src="https://github.com/ability-group/AzureIoTCenter1CMonitor/blob/master/images/AzureIoTCenter1CMonitor-Home.png">

