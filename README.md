Тестовое задание.

Разработка кросс-платформенного приложения (mobile/web/desktop) на Flutter (dart) с использованием системы контроля состояния и базы данных.

Требования:
1. Приложение должны запускаться на трех целевых платформах mobile/web/desktop
2. Адаптивная верстка приветсвтуется (минимальное решение партретный режим с автомасштабирование текста и количества элементов в GridView)
3. Запросы к API должны кешироваться (предусмотреть настройки времени кеширования в настройках сборки приложения параметры окружения)
4. Система контроля состоянием GetX
5. Система управления маршрутами GetX/Beamer
6. БД Isar или аналог (т.к. Isar с WEB не работает)
7. Применяемые паттерны: Clean Architecture/MVVM/etc
8. Приложение д.б. адоптивно для темной и светлой темы
9. Вводимые из браузера пути дожне быть полностью работоспособны
10. Оформление в сите Material Design 3. Картинки не обязательны

Состав приложения.

1) Нижняя панель приложения содержит следущие пункт:
    1. Избранное
    2. Контакты
    3. Кнопка открытия боковой панели

2) Страница авторизации
    Отобржаается для неавторизованного пользователя. Привязывать к FireBase не нужно логин и пароль использовать admin:admin
    Страница авторизации двухшаговая: 
        i. Приветствие и ввод именя пользователя и кнопка далее
        ii. Ввода пароля и кнопка авторизации

3) Не авторизованному пользователю доступня нижняя панель навигации и страница авторизации

4) Страница избранного по умолчанию пустая.
    Если страница избранного пустая - предложить добавить контакт в избранное (кнопка отправялет на страницу контактов)
    Если имеются избранные контакты, то отображается список карточек избранных контактов (на карточке д.б. возможность исключить из избранного)

5) Страница контактов.
    Верняя панель - строка поиска (фильтра контактов)
    Кнопка фильтра - открывает всплывающую нижнюю страницу с облаком тегов контактов. Если кнтактов нет или тегов - кнопка не доступна. Если применен фильтр отметить пиктограммой (индикатором)
    Тело - список карточек контактов (д.б. возможность включить или исключить в/из избранного)
    Плавающая кнопка справа - Добавить новый контакт. Форма добавлени формляется как всплывающий нижняя страницы (ButtomSheet)
    При отсутсвии контакто вывести предложение добавить контакты.

6) Боковая панель содержить кнопку выход

7) Состав карточки контата:
    Фамилия
    Имя
    Отчетство (опционально)
    Номер телефона
    Список тегов

8) Страница "Не найдена". 
    При не корректном вводе не корректного URL в WEB отображется страница не найдена и через 5 сек (можно добавить анимацию обратного отсчета) перевести на главную страницу по пути '/'

Внешние данные.
Первичные данные 

