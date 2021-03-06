# dynatrace-assosiate-dumps
Dump questions from over the internet with russian explanation. 

### What components have built in Built-in static thresholds for problem detection?<br>
  * Dynatrace Self Monitoring<br>
  * Key Request<br>
  * Infrastructure<br>
  * Processes<br>
<details>
  <summary>Правильный ответ</summary>
  
  ### Infrastructure
  * Мониторинг инфраструктуры Dynatrace основан на многочисленных встроенных предопределенных статических порогах. Эти пороговые значения связаны с определением и использованием ресурсов, такими как скачки процессора, использование памяти и диска. Вы можете изменить эти пороговые значения по умолчанию, перейдя в настройки <br> Settings > Anomaly Detection > Infrastructure <br>
  * Для приложений и служб можно в любое время отключить автоматическое определение эталонных значений на основе базовой линии и переключиться на определенные пользователем статические пороги. Если вы зададите статический порог для времени отклика и частоты ошибок на уровне приложения или службы, события будут вызваны, если статический порог будет нарушен. Событие замедления возникает, если статические пороги для медианного или 90-го процентиля времени отклика нарушены
</details>

### What are the discrete concepts for identifying and naming Web request services?(Multiple choice)<br>
  * Web server name<br>
  * Service Type<br>
  * Process Group<br>
  * Service Technology<br>
  * Context root<br>
  * Web application ID<br>
<details>
  <summary>Правильный ответ</summary>
  
  ### Web server name. Context root. Web application ID.<br>
  * Cлужба веб-запросов управляет веб-приложениями, которые вы развертываете через веб-сервер (например, Apache, IIS или NGINX), либо в веб-контейнерах (например, Java, .NET, Node.js, или PHP). Поэтому найминг может быть по имени веб-сервера. 
  * В любом веб - контейнере вы можете иметь несколько приложений в разных каталогах. Например /admin указывает на приложение администратора, а /shop ведет к приложению интернет-магазина. В мире Java это называется контекстным корнем(Context root). Microsoft IIS называет эту концепцию виртуальным каталогом.
  * Некоторые технологии позволяют назначать веб-приложениям явные имена.
</details>

### Dynatrace uses automated baselining to learn the typical reference values of application and services. What are the dimensions?<br>
 * APDEX and load<br>
 * Response times, error rates, and load<br>
 * Response times and load<br>
 * Error rate<br>
 * User experience<br>
<details>
  <summary>Правильный ответ</summary>
 
   ### Response times, error rates, and load <br>
   * Load. Обнаружение аномалий трафика приложений Dynatrace основано на предположении, что большинство бизнес-трафика следует предсказуемым ежедневным и еженедельным шаблонам трафика. Dynatrace автоматически запоминает уникальные шаблоны трафика каждого приложения. Оповещение о всплесках и падениях трафика начинается после периода обучения в одну неделю, потому что базовая линия требует полного недельного трафика для изучения ежедневных и еженедельных паттернов. После периода обучения Dynatrace прогнозирует трафик на следующую неделю, а затем сравнивает фактический входящий трафик приложения с прогнозом. Если Dynatrace обнаруживает отклонение от прогнозируемых уровней трафика, выходящее за пределы разумной статистической вариации, Dynatrace генерирует проблему.
   * Error rate. Dynatrace предупреждает о сбоях. Оповещение об увеличении частоты ошибок начинается после того, приложение или служба работает не менее 20% от недели, то есть 1 день. Обнаружение адаптируется к отдельным версиям браузеров, которые могут показывать либо более высокую, либо более низкую частоту ошибок по сравнению с другими типами браузеров.
   * Response time. Что касается времени отклика, Dynatrace собирает ссылки для медианы (выше которой находятся самые медленные 50% всех абонентов) и 90-го процентиля (самые медленные 10% всех абонентов). Событие замедления возникает, если типичное время отклика для медианы или 90-го процентиля ухудшается. Dynatrace уделяет особое внимание 10% самого медленного времени отклика, испытываемого вашими клиентами. Это происходит потому, что если вы знаете только среднее (медианное или среднее) время отклика, испытываемое большинством ваших клиентов, вы пропустите важный момент: некоторые из ваших клиентов испытывают неприемлемые проблемы с производительностью! Рассмотрим типичную службу поиска, которая выполняет некоторые вызовы базы данных. Время отклика этих вызовов базы данных может сильно варьироваться в зависимости от того, могут ли запросы обслуживаться из кэша или они должны быть извлечены из базы данных. Измерения среднего времени отклика в таком сценарии недостаточны, поскольку, хотя большинство ваших клиентов (те, у кого запросы к базе данных обслуживаются из кэша) испытывают приемлемое время отклика, часть ваших клиентов (те, у кого запросы к базе данных извлекаются из базы данных) испытывают неприемлемую производительность. Уделение особого внимания мониторингу самых медленных 10% ваших клиентов решает такие проблемы. Оповещение об изменении времени отклика начинается после того, приложение или служба работает не менее 20% недели.
 </details>

### The Dynatrace Service Quality report is calculated with which components(Multiple choice)
 * Application
 * Process
 * Infrastructure
 * Service
 * Problem Tickets
 
<details>
  <summary>Правильный ответ</summary>
 
   ### Application. Service. Infrastructure <br>
   * Каждый отчет о качестве обслуживания суммирует результаты мониторинга, собранные Dynatrace за последнюю неделю. Каждый отчет содержит обзор ваших приложений, сервисов, использования инфраструктуры, проблем производительности и влияния проблем производительности на ваших клиентов.
   * Чтобы просмотреть отчеты о качестве обслуживания, выберите пункт Reports в меню навигации, а затем нажмите кнопку Service quality в левом меню. Отчеты о качестве обслуживания расположены в хронологическом порядке, причем самый последний отчет появляется первым. Отчеты включают четыре раздела: общая среда, приложения, службы и инфраструктура. Для каждого раздела рассчитан балл, чтобы показать насколько хорошо ваши компоненты стека мониторинга работали за последнюю неделю. 
   * Overall Dynatrace score  - общий балл Dynatrace, среднее значение баллов приложений, служб и инфраструктуры для вашей среды. Infrastructure score для инфраструктуры и т.д. 
   * Отчеты о качестве обслуживания формируются каждую неделю по воскресеньям в полночь, так что, когда вы начинаете свою рабочую неделю каждое утро понедельника, вы найдете новый отчет.
</details>


### Choose statements that define an Application (Multiple choice)?
 * How software is presented to the end user
 * HTML code running on the browser
 * User experience as measured at the endpoint, such as a browser or mobile device
 * Executable process

<details>
  <summary>Правильный ответ</summary>
 
   ### User experience as measured at the endpoint, such as a browser or mobile device. How software is presented to the end user. <br>
   * Приложения в Dynatrace представляют собой логические конструкции, которые сопоставляются для мониторинга трафика от реальных пользователей(веб-сайт или мобильные приложения). Интерфейс конечного пользователя(endpoint) определяет тип приложения, создаваемого в Dynatrace. Как Dynatrace будет получать данные мониторинга и какие данные будут собираться, зависит от каждого типа приложения. 
</details>


### When are service quality reports generated?
  * Saturday at midnight
  * Midnight every day
  * Friday at midnight
  * Sundays at midnight
<details>
  <summary>Правильный ответ</summary>
 
   ### Sundays at midnight <br>
   * Отчеты о качестве обслуживания формируются каждую неделю по воскресеньям в полночь. Каждый отчет о качестве обслуживания суммирует результаты мониторинга, собранные Dynatrace за последнюю неделю. Каждый отчет содержит обзор ваших приложений, сервисов, использования инфраструктуры, проблем производительности и оценка влияния проблем производительности.
</details>

### What is the maximum number of service calls which are based-lined?

<details>
  <summary>Правильный ответ</summary>
 
   ### 10 000 <br>
   * OUT OF DATE. Устаревший вопрос. Каждая нода кластера Dynatrace может обрабатывать определенное количество вызовов служб в минуту (PurePath или распределенная трассировка состоит из множества вызовов служб). Количество вызовов, которые могут быть обработаны, зависит от количества процессоров и объема памяти, доступной узлу. Как только этот предел нарушен, включается адаптивное снижение нагрузки(Adaptive load reduction). 
</details>

### For Key Transaction How many days is 1h resolution data kept?

<details>
  <summary>Правильный ответ</summary>
 
   ### 400 <br>
   * Dynatrace позволяет вам отображать любой запрос, который он обнаруживает во время мониторинга. По умолчанию подробная история всех запросов сохраняется в течение 10 дней. Долгосрочные исторические данные сохраняются для запросов, которые вы вручную определяете как ключевые запросы. Трендовые показатели для ключевых запросов сохраняются постоянно, однако детализация долгосрочной истории постепенно снижается с течением времени:
   * 0-14 дней: 1-минутного(1m) интервала детализации доступны для визуализации на дашборде и доступа к API.
   * 14-28 дней: 5-минутный(5m) интервал детализации доступны для визуализации на дашборде и доступа к API.
   * 28-400 дней: 1-часовой(1h) интервал детализации доступен для визуализации на дашборде и доступа к API.
   * 400 дней-5 лет: 1-дневная(1d) гранулярность интервала доступна для визуализации на дашборде и доступа к API.
</details>


### What is the maximum number of nodes allowed in a cluster(Dynatrace Managed, 2020 year)
  * 64
  * 10
  * 24
  * unlimited
<details>
  <summary>Правильный ответ</summary>
 
   ### 24 <br>
   * Кластер можно расширить горизонтально, добавляя больше узлов. Поддерживается установка до 24 узлов в кластер.
</details>   

### Time series data is held at a resolution of 1 day for how long?
  * 1 years
  * 2 years
  * 5 years
  * Depends on disk size
<details>
  <summary>Правильный ответ</summary>
 
   ### 5 years <br>
   * Dynatrace позволяет вам отображать любой запрос, который он обнаруживает во время мониторинга. По умолчанию подробная история всех запросов сохраняется в течение 10 дней. Долгосрочные исторические данные сохраняются для запросов, которые вы вручную определяете как ключевые запросы. Трендовые показатели для ключевых запросов сохраняются постоянно, однако детализация долгосрочной истории постепенно снижается с течением времени:
   * 0-14 дней: 1-минутного(1m) интервала детализации доступны для визуализации на дашборде и доступа к API.
   * 14-28 дней: 5-минутный(5m) интервал детализации доступны для визуализации на дашборде и доступа к API.
   * 28-400 дней: 1-часовой(1h) интервал детализации доступен для визуализации на дашборде и доступа к API.
   * 400 дней-5 лет: 1-дневная(1d) гранулярность интервала доступна для визуализации на дашборде и доступа к API.
</details> 

### For a new application must run for at leave X% of the week before alerting (workload spikes/drops) will take place. What is X?
<details>
  <summary>Правильный ответ</summary>
 
   ### 100 <br>
</details>  

### How long is time series data held with a resolution of 1 minute?
 * 14 days
 * 7 days
 * 1 day
 * 1 hour
<details>
  <summary>Правильный ответ</summary>
 
   ### 14 <br>
   * Dynatrace позволяет вам отображать любой запрос, который он обнаруживает во время мониторинга. По умолчанию подробная история всех запросов сохраняется в течение 10 дней. Долгосрочные исторические данные сохраняются для запросов, которые вы вручную определяете как ключевые запросы. Трендовые показатели для ключевых запросов сохраняются постоянно, однако детализация долгосрочной истории постепенно снижается с течением времени:
   * 0-14 дней: 1-минутного(1m) интервала детализации доступны для визуализации на дашборде и доступа к API.
   * 14-28 дней: 5-минутный(5m) интервал детализации доступны для визуализации на дашборде и доступа к API.
   * 28-400 дней: 1-часовой(1h) интервал детализации доступен для визуализации на дашборде и доступа к API.
   * 400 дней-5 лет: 1-дневная(1d) гранулярность интервала доступна для визуализации на дашборде и доступа к API.
</details>  

### The baseline cube is calculated X hours after your application or service is initially detected by Dynatrace OneAgent. What is X?
<details>
  <summary>Правильный ответ</summary>
 
   ### 2 <br>
   * Dynatrace проверяет, когда ваши приложения и службы обнаруживаются агентом OneAgent. Базовый куб вычисляется через два часа после первоначального обнаружения вашего приложения или службы, чтобы анент OneAgent мог проанализировать два часа фактического трафика (предварительные значения откуда исходит ваш трафик). Расчет связанных значений куба(reference cube) повторяется каждый день, чтобы Dynatrace мог продолжать адаптироваться к изменениям вашего трафика.
</details>  

### Choose statements that define a host(Multiple choice)?
  * Physical hardware
  * The source of compute, memory, and storage resources
  * A physical or virtualized operating system
  
<details>
  <summary>Правильный ответ</summary>
 
   ### A physical or virtualized operating system.The source of compute, memory, and storage resources. <br>
</details>   

### How long is time series data held with a resolution of 5 mins?
<details>
  <summary>Правильный ответ</summary>
 
   ### 28 <br>
   * Dynatrace позволяет вам отображать любой запрос, который он обнаруживает во время мониторинга. По умолчанию подробная история всех запросов сохраняется в течение 10 дней. Долгосрочные исторические данные сохраняются для запросов, которые вы вручную определяете как ключевые запросы. Трендовые показатели для ключевых запросов сохраняются постоянно, однако детализация долгосрочной истории постепенно снижается с течением времени:
   * 0-14 дней: 1-минутного(1m) интервала детализации доступны для визуализации на дашборде и доступа к API.
   * 14-28 дней: 5-минутный(5m) интервал детализации доступны для визуализации на дашборде и доступа к API.
   * 28-400 дней: 1-часовой(1h) интервал детализации доступен для визуализации на дашборде и доступа к API.
   * 400 дней-5 лет: 1-дневная(1d) гранулярность интервала доступна для визуализации на дашборде и доступа к API.
</details> 

### What percentage of CPU consumed by the oneAgent does dynatrace, start to limit network monitoring?
 * 2.5%
 * 0.5%
 * 5%
 * 1%
<details>
  <summary>Правильный ответ</summary>
 
   ### 5% <br>
</details> 

### What is the port for communicating from agent to ActiveGate?
<details>
  <summary>Правильный ответ</summary>
 
   ### 9999 <br>
   * По умолчанию порт 99992. Может быть вручную перенастроен в файле ActiveGate custom.properties.
</details> 

### What are the characteristics of a service (Multiple choice)
 * How software is presented to the end user Related terms: Browser, User Action, Session, JavaScript, Waterfall
 * A set of code that accepts requests and returns results
 * The result of instrumenting a process
 * A means for code to request computing resources
 * The “code layer” which requires “deep dive”
<details>
  <summary>Правильный ответ</summary>
 
   ### A set of code that accepts requests and returns results. The “code layer” which requires “deep dive”. The result of instrumenting a process. <br> 
</details> 

### Can you mix servers of different hardware specs in a cluster?
<details>
  <summary>Правильный ответ</summary>
 
   ### Нет <br>
   * Все ноды в кластере должны иметь одинаковую аппаратную конфигурацию.
</details> 

### Key Requests get special privileges these are(Multiple choice):
 * Better Searching - think tagging
 * Historical data guaranteed – data kept in Cassandra
 * Custom thresholds – think SLAs
 * Always baselined by AI – more on that during problems
<details>
  <summary>Правильный ответ</summary>
 
   ### Custom thresholds – think SLAs. Historical data guaranteed – data kept in Cassandra. Always baselined by AI – more on that during problems. <br>
</details> 
