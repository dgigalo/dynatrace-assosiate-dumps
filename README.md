# dynatrace-assosiate-dumps


What components have built in Built-in static thresholds for problem detection?<br>
  * Dynatrace Self Monitoring<br>
  * Key Request<br>
  * Infrastructure<br>
  * Processes<br>
<details>
  <summary>Правильный ответ</summary>
  
  ## Infrastructure
  * Мониторинг инфраструктуры Dynatrace основан на многочисленных встроенных предопределенных статических порогах. Эти пороговые значения связаны с определением и использованием ресурсов, такими как скачки процессора, использование памяти и диска. Вы можете изменить эти пороговые значения по умолчанию, перейдя в настройки <br> Settings > Anomaly Detection > Infrastructure <br>
  * Для приложений и служб можно в любое время отключить автоматическое определение эталонных значений на основе базовой линии и переключиться на определенные пользователем статические пороги. Если вы зададите статический порог для времени отклика и частоты ошибок на уровне приложения или службы, события будут вызваны, если статический порог будет нарушен. Событие замедления возникает, если статические пороги для медианного или 90-го процентиля времени отклика нарушены
</details>

What are the discrete concepts for identifying and naming Web request services?(Multiple choice)<br>
  * Web server name<br>
  * Service Type<br>
  * Process Group<br>
  * Service Technology<br>
  * Context root<br>
  * Web application ID<br>
<details>
  <summary>Правильный ответ</summary>
  
  ## Web server name. Context root. Web application ID.<br>
  * Cлужба веб-запросов управляет веб-приложениями, которые вы развертываете через веб-сервер (например, Apache, IIS или NGINX), либо в веб-контейнерах (например, Java, .NET, Node.js, или PHP). Поэтому найминг может быть по имени веб-сервера. 
  * В любом веб - контейнере вы можете иметь несколько приложений в разных каталогах. Например /admin указывает на приложение администратора, а /shop ведет к приложению интернет-магазина. В мире Java это называется контекстным корнем(Context root). Microsoft IIS называет эту концепцию виртуальным каталогом.
  * Некоторые технологии позволяют назначать веб-приложениям явные имена.
</details>
