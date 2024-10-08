## Интеграция с Мегаплан <br />  

Решение позволяет передавать в наш кабинет данные по сделкам, для дальнейшего построения Сквозной аналитики, а также интегрировать функционал телефонии и передавать данные по звонкам в Megaplan. <br />  

 **Какие данные передаются**   <br />  

 Данные получаемые по сделкам:    <br />
- сделки: сумма сделки, валюту, товары/услуги и тд;  
- воронка продаж и ее этапы;  
- контакты;  
- ответственный менеджер.  <br />  

Данные передаваемые по звонкам:  <br />

- всплывающая карточка контакта при звонке сотруднику;
- прослушивание записанных разговоров прямо в личном кабинете Мегаплан;
- сохранение всей истории коммуникаций с клиентом в его карточке;
- автоматическое соединение клиента с его персональным менеджером;
- исходящий звонок по клику или звонок из виджета;
- автоматическое создание контакта при любом звонке;
- создание задачи на потерянные входящие и неуспешные исходящие звонки;
- возможность создавать коммуникации по выбранным типам звонков;
- синхронизация с режимом “не беспокоить” веб-телефона Мегаплан;
- переадресация на ответственного из CRM, при настройки соответственного сценария в ЛК <br />
<br />
<br />
<br />
<br />

## Подключение передачи сделок   <br />


<details>
 <summary style="font-weight:bold;"> Шаги по подключению </summary> <br />


1. Укажите **Учетные данные** <br /> 

Для авторизации в мегаплан необходимо: <br />  

- нажать "Авторизация в Мегаплан";
- если ранеее добавляли учетные данные Мегаплан, то выбрать их из списка, если нет, то нажать "Добавить учетные данные";
- заполнить значения:
  - название;
  - логин(username) и пароль(password) от Мегаплан;
  - домен Мегаплан в формате https://mp361546.megaplan.ru , часть 'mp361546' будет у каждого клиента уникальной.
    
После добавления учетных данных на странице появятся Параметры интеграции.

2. Нажмите **Активен** на этой странице. <br />  
3. Создайте приложение в Мегаплан на Webhook url сервиса UIS из настроек.  <br />  

![image](megaplan_app.gif) 
<br />  

4.  Нажмите сохранить <br />  

После подключения интеграции сделки будут попадать в  Сырые данные -> Сделки.  <br />  
Для проверки корректности работы интеграции создайте тестовую сделку в Мегаплан.

</details> 

<br />
<br />
<br />
<br />
<br />
<br />
<br />

## Подключение телефонии   <br />

<details>
 <summary style="font-weight:bold;"> Шаги по подключению </summary> <br />

1. Укажите **Учетные данные** <br /> 

Для авторизации в мегаплан необходимо: <br />  

- нажать "Авторизация в Мегаплан";
- если ранеее добавляли учетные данные Мегаплан, то выбрать их из списка, <br /> 
если нет, то нажать "Добавить учетные данные";
- заполнить значения:
  - название;
  - логин(username) и пароль(password) от Мегаплан;
  - домен Мегаплан в формате YOURDOMAIN.megaplan.ru, часть 'YOURDOMAIN' у каждого клиента уникальна.
    
После добавления учетных данных на странице появятся Параметры интеграции.

2. Нажмите **Интеграция активна** на этой странице. <br />
3. **Фильтровать по виртуальным номерам** - выберите настройку, если требуется  фильтрация по виртуальным номерам (в случае подключения нескольких сетей/интеграций). <br />
При прожатии будет выведена дополнительная настройка с выбором виртуальных номеров. <br />

**Список виртуальных номеров** - укажите виртуальные номера, по которым необходимо отображать данные по звонкам в Мегаплан в подключенной сети. <br />

4.  Выберите настройку **Включить переадресацию на персонального менеджера**, если необходима переадресация на персонального менеджера из CRM.  <br /> 

**Важно:** переадресация на персонального менеджера из CRM будет работать при настроенном сценарии с соответствующей операцией в Novofon , а также при соответствии внутренних номеров сотрудников в Novofon и в разделе "Телефония" в Мегаплан (подробнее в п.8).  <br /> 

5.  **Ответственный по умолчанию** - если звонок потерян или поступил на сотрудника, который отсутствует в Мегаплан, то выбранный сотрудник будет назначен ответственным при автоматическом создании контакта.<br />

6.  **Создавать контакт при звонке** - настройка позволяет создавать контакт в разделе "Клиенты" при начале разговора. <br />

При её выборе выводится дополнительная настройка выбора ответственного сотрудника. <br /> 
**Назначать ответственного на** - выберете кого назначать ответственным за успешный звонок от нового клиента (последний или первый разговаривавший). <br />
   
7. **Создавать коммуникацию по звонку** - настройка позволяет создавать коммуникации в разделе "Клиенты" - "Коммуникации" с типом "Звонок" после завершения звонка. <br />
При её выборе выводятся дополнительные настройки передачи коммуникаций: <br />
  - **Создание коммуникации по типам звонков** - добавьте необходимые типы звонков, по которым необходимо создавать коммуникацию в требуемом статусе. <br />
  - **Длительность коммуникации** - укажите время в минутах, которое необходимо добавлять к времени начала коммуникации, при формировании времени окончания. По умолчанию указано 120 минут (2 часа). <br />
  
8. В **Мегаплан** заполните настройку телефонии: <br />  
 -  Под пользователем, который входит в группу «Директора» или «Админы», зайти в личный кабинет Мегаплан.
 -  В аккаунте выбрать раздел «Расширения».
 -  Найти приложение «Телефония Новофон» в категории «Телефония» и установить его.
 -  Теперь необходимо указать для каждого пользователя Megaplan внутренний номер виртуальной АТС UIS. 
    - Для этого открываем интерфейс CRM-системы, переходим в раздел “Настройки”, открываем вкладку “Интеграция”, в меню слева выбираем пункт “Телефония”. 
    - Обращаем внимание на блок “Подключение к телефонии по API” и там нажимаем “Настройки телефонии”. 
    - Переходим на вкладку на “Пользователи”.
    - Добавьте всех пользователей, использующих телефонию. Для каждого из них укажите внутренние номера АТС из раздела "Сотрудники".  <br />
    ![image](megaplan_telephony.gif)
    **Важно:** если сотрудник не будет указан в данном разделе, то функционал поднятия карточки звонка и передача информации по нему не будет доступен. 
    - Нажимаем сохранить.  <br />
     
9. Нажмите кнопку "Синхронизировать настройки телефонии из Мегаплан". <br />
10. **Синхронизировать сотрудников** - настройка позволяет импортировать выбранных сотрудников из Мегаплан в UIS. Связь сотрудника в UIS с сотрудником из Мегаплан происходит по e-mail.
При прожатии будут выведены дополнительные настройки:
- список сотрудников из Мегаплан. Необходимо выбрать тех сотрудников, которых требуется создать в UIS.
- кнопка"Синхронизировать", для принудительной синхронизации сотрудников. По умолчанию синхронизация происходит каждые 2 часа.

    
12. **Обработка потеряных звонков**- при потерянных звонках можно настроить автоматическое создание дела как на входящий, так и на исходящий звонок. Дело будет создано только, если существует контакт клиента.
    - **При входящих звонках** - вы можете включить автоматическое создание Дела при потерянных входящих звонках и задать кто будет ответственным за него: менеджер из карточки контакта в Megaplan или ответственный сотрудник по умолчанию. <br />
    - **При исходящих звонках** - вы можете включить автоматическое создание Дела при потерянных исходящих звонках и задать кто будет ответственным за него: менеджер из карточки контакта в Megaplan, ответственный сотрудник по умолчанию или сотрудник, совершивший звонок.

   
13. **Номер для звонка по клику** - номер, который определяется у клиента при звонке от сотрудника, у которого нет зарегистрированной SIP-линии.
14. **Переопредeлять АОН для исходящих звонков** - выберете настройку, если требуется для всех исходящих звонков по клику отображать клиенту только выбранный номер в параметре "Номер для звонка по клику".
15.  Нажмите сохранить <br />  
   
 </details> 
