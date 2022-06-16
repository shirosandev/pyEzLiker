# pyEzLiker
Библиотека для работой с api https://easyliker.ru

Установка и инициализация : 
--------------------------------------------------------
<h4>Установка</h4>

    pip install pyezliker

<h4>Инициализация</h4>

    from pyezliker import EasyLiker
    
    ezliker = EasyLiker(token)
    

Получить баланс профиля : 
--------------------------------------------------------
    >>>> ez.get_account_balance()
    >>>> 78.4
 
Получить список доступных сервисов: 
--------------------------------------------------------
    >>>> ez.get_services()
    >>>> # Огромный словарь с сервисами.
    >>>> ez.get_services()['youtube']
    >>>> # Доступная накрутка для ютуба
    >>>> # Пример с лайками: {'quality': 'offers_medium_quality', 'price': 0.4, 'description': 'офферы, среднее качество', 'min_limit': 20}
    
Сделать заказ: 
--------------------------------------------------------
    >>>> # Взял лайки из примера выше
    >>>> ez.create_task(website="youtube", type="likes", quality="offers_medium_quality", link="https://www.youtube.com/watch?v=bj4ul946k2o", count=150)
    >>>> {'id': 477515, 'link': 'https://www.youtube.com/watch?v=bj4ul946k2o', 'price': 60.0, 'balance': 78.4, 'status': 'Выполняется'}
![image](https://user-images.githubusercontent.com/73769205/174016929-3f0bdfc1-68e7-4b99-a5b6-f74a7cddbbb6.png)

Получить список заказов: 
--------------------------------------------------------
    >>>> ez.get_tasks()
    >>>> #Список заказов, которые вы совершали (я сонный, хз как уже перефразировать)
    >>>> # Можно так же получить информации по нашему прошлому заказу
    >>>> ez.get_tasks(id=477515)
    >>>> [{'id': 477515, 'creation_date': '2022-06-16T10:17:00.126647', 'name': 'Youtube лайки | офферы, среднее качество', 'link': 'https://www.youtube.com/watch?v=bj4ul946k2o', 'sum': 60.0, 'count': 150, 'done': 0, 'status': 'Выполняется', 'date': '16.06.2022 | 10:17:00'}]

![image](https://user-images.githubusercontent.com/73769205/174017447-b810ee8a-b2c2-4659-81f4-b972f7b02ce3.png)
