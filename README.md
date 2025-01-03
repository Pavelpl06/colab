# User case
***Диаграмма вариантов использования для приложения по съёму жилья***

![Снимок экрана 2024-12-18 105018](https://github.com/user-attachments/assets/f6f17ee7-e0af-4537-9662-cacb27c643d2)


## Final work


***Программное обеспечение для автомата, печатающего фото из Instagram.***

Требования для автомата печатающего фото из instagram

Глоссарий

Требования функционального характера
+ БТ- бизнес требование
+ ПТ- пользовательские требования
+ ФТ- функциональные требования

Требования нефункционального характера
О- ограничения

Требования функционального характера

- БТ001 Необходимо разработать программное обеспечение для автомата печатающего фото из instagram,в котором пользователь сможет распечатывать фотографии с мобильного телефона и с аккаунта в instagram
- ПТ001 Пользователь должен иметь возможность просматривать фотографии с аккаунта instagram 
- ПТ002 Пользователь должен иметь возможность просматривать фотографии с мобильного телефона
- ПТ003 Пользователь должен иметь возможность распечатать выбранные фотографии 
- ФТ001 Система должна предоставить возможность ввести свой логин  аккаунта instagram
- ФТ002 Система должна предоставить возможность соединить телефон  через кабель зарядки
- ФТ003 Система должна предоставить  два способа “Выбрать фото для печати” - выбрать фото в instagram или загрузить фото с телефона

Требования нефункционального характера

О001 Пользователь не должен иметь возможность распечатать более 100 фотографий




***Диаграмма вариантов использования для “Автомата печатающего фото из instagram”***



![Снимок экрана 2024-11-12 134608](https://github.com/user-attachments/assets/3bee6786-05c6-4d62-b5cc-79f07463ce33)



***Описание варианта использования “печатать фотографии”***

ВИ-1. Печатать фотографии

Краткое описание:Потенциальный клиент воспользовался автоматом для печати фотографий из instagram  

Действующие лица:Клиент

Предусловие:
- У клиента есть своя страница в instagram
- У клиента есть с собой зарядное устройство и мобильный телефон

Основной поток

* Клиент выбирает печать фотографии на сенсорной панели экрана автомата
* Система предлагает на выбор два варианта-  выбрать фото в Instagram или загрузить фото с телефона.
* Клиент входит в аккаунта instagram,либо присоединяет мобильный телефон к автомату через кабель зарядки  
* Если профиль пользователя открыт , то управление переходит на следующий шаг
* Пользователь выбирает фотографии из аккаунта instagram,либо с телефона
* Система позволяет выбрать не более ста фотографий
* Клиент выбирает “распечатать фотографии”
* Система распечатывает фотографии
* Вариант использования завершает свою работу

Альтернативный поток:

4а. Если профиль пользователя закрыт
- Система отображает уведомление  о закрытом профиле
- Управление переходит на шаг 2

Постусловие:
В случае успешного выполнения основного потока клиент распечатывает фотографии
Результат:
В случае успешного ВИ выбранные фотографии распечатаны.

 
