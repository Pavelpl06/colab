## User case 

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

## ***Диаграмма последовательности***

 [Снимок экрана 2024-11-07 215121][def]
 

## ***Итоговая работа по SQL***

[Итоговая работа по SQL](https://github.com/Pavelpl06/colab/commit/e12664fd14913b8aab5cebd6b99fd27fa916837a)


## ***Прототипирование интерфейсов***

[Приложение по учету расходов](https://www.figma.com/proto/WFhD7P91ZIphH8QGEx4Jrt/Untitled?node-id=43-81&p=f&t=XO21db9BxpriMPmY-0&scaling=scale-down&content-scaling=fixed&page-id=0%3A1&starting-point-node-id=4%3A2)

## ***Моделирование бизнес-процессов***

[Салон красоты](https://viewer.diagrams.net/?tags=%7B%7D&highlight=0000ff&edit=_blank&layers=1&nav=1&title=%D1%81%D0%B0%D0%BB%D0%BE%D0%BD_%D0%BA%D1%80%D0%B0%D1%81%D0%BE%D1%82%D1%8B0210%20(1).drawio#R7V1bc6M4Gv01rpp9mBTizqNvmdmt7q2u6t3anUdiE5ttbDKAO%2FH8%2BhUXyUIIcwkgkairywEZMCDpnO%2BuhbY%2Bvf0WuS%2FHr%2BHeCxaqsn9baJuFqmqmbsI%2Facs1b1EdRclbDpG%2Fz9vAreG7%2F5dXNKLDLv7ei0sHJmEYJP5LuXEXns%2FeLim1uVEUvpYPew6D8q%2B%2BuAev0vB95wbV1v%2F4%2B%2BSYt9qqdWv%2F3fMPR%2FTLwHTyb04uOrh4kvjo7sNXoknbLrR1FIZJvnV6W3tB%2BvbQe8nPe6z5Ft9Y5J2TNif8DJ2v5z%2Bf%2F304bX9%2Bef79n1c%2F%2BsevxVV%2BusGleODFRlksQfq5UrLPVfa5zT7hAXnjcrEBC1tBh8FtgA6D22r2uSqeO7milxm%2F%2BqfAPcO91TE5BbARwM3d0Q%2F2X9xreEmfI07c3Q%2B0t4q8GA6Jb%2BghAdX01U1HmpJeL4z8v8Jz4gZFA7xOlBTjSS0f8T39ieKw16OfeN9f3F163CscxLCt%2BmbRa%2FKixHsjmoo3%2FZsXnrwkusJD0Ldm0etXNC6K%2FdfbINLxQUdyBCl60eoWQ%2FeAr37rXbhRdHCHztaYne3kvahnn%2Bvs0y46u9jOexf3K9nrKtHrSsv%2BvtMzRadUO%2BDu4G3dKyqrE3RGJ1jGWH0AQOUteXuIOMVuGCXH8BCe3WB7a11F4eW89%2FbF27kd8yUMX4qX%2Bj8vSa7FS3UvSVh%2B5fA9Rtf%2FFudnO3%2BkOw8G2t28kV9uruTeNy%2Fy4cN7UbfeKUZbHF6inXfnuAIv4aA4eHd7u%2BiS9HXd7ezIC9zE%2F1kG8OE7UtV59OTejY%2FZ%2BXgmLVOWgw1PQZiiWt746AcB7sM9OiT8mU6xtIX4fpzuHK6XilO%2FhT68vxvAAqMEsL%2Ba1IzNx1NxFtXX%2BDb6d7%2FDxtIlQZk5ihoISzO0LOgzZ1NQA6c2uggG3seFagYpHz5FcOuQbmXH5BfE7MskbGqMvqRvJHtHxgr%2BVx6ADt%2FkGv9dGPCodfZNvl9usw320SBrpa%2BAji7%2BUtcGVBu6k8rR5WvD%2F3CUH92X9IlOb4dU8nx4ejmdH7yf2Rgm50tKDj4U5764T17wLYz9xA%2FP6WwJkyQ8wQOC9IsVFAgO2dxch0EYZW9Ke87%2BEddYBv4hPTdJ5%2BrKLfZ28DdTbFy9EDgJRxCUUD0COldQoAn8s7fGgmo6%2Bdz4Jd959t%2FSaY2OygWh896N0sb4enoK0yc6eXGcCawdZ217inTKcotmGRXKNBiEOR5fapUR%2FMn5EvFgM2GqYhGmwoZMmxA%2Fy2B5Ez91Ytsktkk0Vcs4Cj%2FXhLZyF5XzExuRUmUBIqvNqjbm%2BKg2g2beZtF4abEAk9WmMhqZl2QBNnWT9UibuPGPGu0pgoCGpieeiKs4n2pAoXS%2FVOyHeBehiff2AlGvmDi7MAjcl9h%2Fyq6VtqQ%2F%2B9WNfmTHu09xErkpeq78OJ3a3y9PxWXGQkesQSB4NKsaBVAZ%2BGiPho%2BGxEc27DXjoy4WPqpsfHysQTqDaLdZqLepyIT5YVYJB4uDLeLgx7Lin20XcqYmIfUjQ%2BolzkTVseBTFw8%2BLfak02sG8KTYeoPTP0poyhFb9bbYagqFrchWQ3fzhkBSlUdn8%2BofVROqf0BN%2FxgV4zNmtxVBTPf5KztLe2xLRjSj3OOjNuyDj60QUC3XNDFLPYkc3MR7da%2BqEEaQ6Bieni5xoxHkZvM4h5mzANs7iv3D67%2Bu2bN6b7vgEmfDcTSSMoFoJhCzm2C4JRRqpmC4LFsNHwkQNAmBrio5khOxapeRwp3Ywt3JPV8y%2B%2F9YM8dAM6WYOYbOW7xDbvoZa8fem58Q0iDc%2B4P45naldOdK7IwsCSIBolnSMISSNFT7g44IMJ8RIZZuALQ%2BIIFQvog7SsWlgZ27NTLZ3nt2L5kvME6i8IdXbX%2BGHPHonvwg7fzfveCnlwpuxRfFbwNQ7LMuSziVC4%2FxHZ8ycjuP6lQeXl1he5Uth69XWa0J0blvAwQlf4mKlSB8ikGoSCwzHe1W2Up1aRbqEtNFfEmDI4MxNSTLEkxD0jgb6sRzgiCpq5mMB4%2FXeacTpI8%2F65OQsSARXsNL9GwydhTOZGywyRj7BtYsrm2kZxmPNc94rJ2b7I7%2B%2BbCYNB7Ltstci20l3LiWi59EaK41W3KtBgTjWlNyrehcO7itpIZrqXyVybm2xsdBOWip2BZjwQh10QsalkQribYL0VKRz7rFm2g5Rz6LF32CdNW5ES26b%2B5WPemxlR7bcpqqQgU7qGbVlDety7aXN%2BZD6xcIzZphTyzHGrpvEvakU0F4p4IIMVhA0cu2P%2F7SmCOSNAZEgKXWZg9bKFjSuWTg83r5KARLlJcv0zl796QqVE9qNRYbVPtlkye4k9VBumQOyQCEOcgK3rkUe3DwoJ4zrsJCZ2ByFwyM%2BRd0ETTEFMkNjchoi8VxoFfUsfSrTOlXGV4mZftVgEopMlM7VtCD0jStEdSsViyQG%2BJbZvbV%2FXThchGG5jI2yH2Dk4xvl1qhFrittU08kZ6d%2BXh2IN7tsyeYVm7QDM5yA1D7WBQkS0zJEsMrzzUsoVFm%2BKlZAj0ozRImoZ%2BtCMjflLQ3tex4zzjhgdD1toR%2BBwg8XxEEwXRayYA5ifY90R6U5pOpcEZ7htTyyZ35yJzVrN2JZfcCvTIIJW9PytuDD5k63jY487bK5m1Sr1sSvG0hrkYHNGpckn1nyr5P6e38PXueqdmXnhX8bbTz9zohGy1K8yYuxdNGi7qskcWNqSDZMJwHh%2FhXNr%2BpQHlQDNuG%2Br%2Fq6AA4evkH8gceDa%2BNGj2rizmtWwG%2Bcnz0UAY2GScoVJzgyGX7gFadRRVAnzZK0OiTuiIWog%2BNxG31KWPw9M339WSNCGthyAJlAxMJc%2BsFZXtqW81USrXzlGpZNqUEXm1U%2BDOo1BAVZQbzkmdNlQf6DQ1YRkvAMsXK5gCaNACJXi9oeI6r0TYsh68BCD0oI7UIO16sSm1IcmWvrmpFUQT8F4p2c9XBQBqGQhCw9TepUMxMobiztEK%2B%2FzWtMvTd%2B7MXNXSgXkujqJe%2F5sGoGC7FyZmKkywjqQeJqoM4iRG47xJLKICUGNEo2YQc0Kht8AFtcc5sEVCVbh14OvgKIjVihmndM2qa1sRCR01MIel1Wpdlhzpxo6lsuxQc5iU4jG2JNOnwfwS%2F3OQB85MsLYG08GZ1XaylJWxpKe7bk7ZYlmLQq8znJzG8CBJ5M7ytji0RqQrn9X%2FRg%2FZcAJi0z%2BiE2FRd2k0nLgV7y3RPKaGfn%2BKXrPeY%2BRRyMZyPkFwpRCEGRzjfBxc%2BHxom266VYIpGwX2yXSUFT0rBE62VoALOSSvoQWsrEGQZhze3%2Fx0zBFlWrbpI6qa89Gl9cG0RsSBtFrOyWYxfZc0xysIqf6uFVRN181iRP0kTHkoI5qlQ4x2BFOq2kQyWWGxu1ZiuMKhhmDNQeKhyK%2BdCY6VBQO0SxVk1IaYcSf1Gkjn4sh3ZqVBOca%2FEAQV13ZEBqKVgzKKQ82PbE%2FQiM6%2FuBFCpy9v5hMJbcpsp%2BVMOK4vUx2HcFyzIKO0mwUKq7VJtb6220wmwVS%2FzpGq71cd2K5za3rYAtSFWyUN0390cthiX3h1NLUFJglLKzJTBgHteoMW5dpt4Wfkouo2DAPq%2BnuRcNVy88rwWP1XifT3JeYHmGfekYHUQLYZOJEWF2YsKcFy7QeCNajClJQX%2B9XuEkhREQCUENs26kFiohO5botKHQqVJFBidykbRTN6wxHDjNA5mmYwiZjIKVUwdXuTkn%2BGsVccc0nStHpzrzG1IM5xSckjLId0hZ5DKETAY3vZphzQXlXZoea%2B1FmqJJe%2FVeOawURssbDLGdlkybd%2B8d2R59GpBJnzKlvCUr4iDAfETBjKst6zh1E46bS2aMjBPxhPNJwcKiqGi5UTbMidacva7xrRG5%2FnzDjNHhQFnnDbGXtYHFZDkVjISKG1XPHOmimQ26ZR8hxpWI5eFRPncH26wKTMabCqvwaZPO9iAwqUa7sAdi7qrsV%2BBMnjHvjOFpiobyRQasVJoJsMCG4k5nFJo0IPSyrHeVvWUQryYQjyrsNHJi2P3MKaDBGqYVISXXlVNpxXjucQFDQ1HbbNFHVMwqusjaUiqm5TqptKx6LSMtlTXOSWF5lTDup8wUrkz6oRxEkbQe%2B9WNkjyr%2BTfLvxrKpzNaABwLr8kXuCU09YiAVCJG0HoHN14bRYJVfcXO8So5R2p3PsN4fjSKpmnNuF2Q3n46ecWud3ILGXsVSMXkcwPlj60WfnQ7hQgHgs8NV2vsQJz86sBlLU3Y8Pw0OjZtjYrQFQoCnrWFE2lMoQxzD2ysHJL5OCtKpAqF26SMNcMc3RsvYEqZHKEuT4x2VL1EVP14RE%2FoCuVhBHO%2Be4AaV6SuiueuBbcPXhh9Xd2Zo2f5LGigugEN%2BdsTSoiTNWn07KPpDploUJnmYYkuX9e3D962THVoRQanRFUNTXTc87uFREV9daoKFZkNb7zIVGxUkLsdvqyXIaRWtMWED%2BBf5QwF6WfDnFNB12HtDNZpbuSiCoRtaw7VaqX8UdUtC6Q9LEKuxohDkIc3clqUf6fqeOJ8JPK7OpZZVdzcleaqEQIHQrLz13JJTZWbPm0bUkoAIBY8in4qDkcAoTVtx8UYrlhcPKclJcElpcGV3TZ8pKmq%2F3kpa5BaZUfAkV91rqgNHgCYN7ZqEFp%2BMXf0%2Bi3hEq%2BJZTuO3bOLYoHIfX0XDcnTyTzqxVivYZMo5fFj6UgWauX63RlUe6CpNqHZkQLPMfk3YLmxaoiCbQ%2Bst8noXlBQs9HEA1ryNTU%2BKZZ4ScdjFdlcMQ8gyM48aNJ8aOm8uZHwLlg82i6Of%2F6CsgMM7sAc4BgWpK2wKQ9uJGvjrR7JowNR9qATdrkchjUer3w05Z0Lel6YLrmr86Cj1DCEPNdcyK1WOv34BuXbtVZWcNEKFqtWXS8P6Nc4MS2sRpivZPd0kipn3zdHmx%2Fm5%2FQj6Csv23EYLgLhvE8ZHlYfIeaVR5rKaLOabhp46gLnR1wFmUCBM79qhAAUBUpO5%2BgF%2Fl443rsUEdIyeBDSQYTLLJTEQy4GwXZ4eRLQIgFRjm3HyP2ikBsUBO%2BHb%2F6p8DN3jMxZDJ7SgHEahaMHEb%2BX2kUckcLCujaAVRIgGVUX7%2BOw1XIDlDp8qTD9QBDz2Bz8ZLY3hCvXSNIdl2R3hpLqZuZ4espgluHdIv4LVkm%2FXNH6%2Btd5xcAKLO5mGF2dYJNHKxfXwOATO6n6gGQNka1hHC3b%2B%2BtTvALgZ9bIs2FzD4kp%2FOaoW7dfvXxbwuccdNhGQN0aTlL5Swts6BGZSlyn6U6l5JV3aSMRg0NvdRGBQ1RviDmAP3TLOTbuifbGq2HV7Xf1ZMMRXSKnhzIKS%2FyiACtK8gN7saoyTujw5sdQIHzQHHUJlrKC%2F2Ocd8oU72x8gnjGGXQC5xxbEt1xLYenG0LdKGeEQSunM%2FcaWpbaWG6VFZbL091nCs4UfgHeiVsJ9WS0J0sptbVTjPCBQ1wpYKql0KTxd0%2BmurU3VZI%2By8cRkjIxMYMtaaEddOg72mXzWLmirPYb79iuUVX%2FpIb3bOr%2BEGArP6F0Z01SAboMmCWRY9fmfZdk9FluB7eCNmPNa53ss5K1Xhjl1fJpKrrtlkfs7cVlxgczZZ6YviwOvWd4ZhDjAmqfghQreqgcFg2f23EMSFMqsyg0pAQUbvIz1cftLsL3Dj2dwsybreLPUhvLZjralshTx98UYh3jlC1ilqN0pCMqRUzphbOhfPejUpFQg8eFLEyWWlwjG7gwdbQTSE3ozb4tEF0vazUErXnh9ptF38Cglny8Z3fy5%2BgAguoldfLEuRSv4mqzhaJlTZSn1VCpsRlALHYiiIVsK4tl2D%2FDKq3sHSiUpXakHWLnzqv90nxkIQyP0Jp608EumD1Zuui08ii2ct3GyBQYp9KrmJEWnqrSaqSDsSmg0ucaSrCkgFdvoY%2FGSC9pe3CwJIpPiJTtC7ypwtW%2FcdgGIw2jatrchrEMx93PNLiRhnExkSVDUyDcgLQMD52YQO9pspfo%2BOuumqJw%2FAbyUp9HyEDicxNFlZwMunwLt5WWUP60gSkqBFYpXW6tSGaL42RMHoTjepRXfrbZupvS45wcvjnw2Jm%2FjZNNGiv2n24Q%2FsAsekS2mvUgPlBO7rzew43UgMGpRCvIa2kMl5VWkkHZwTDLofAYhcaRzMpw8UtBaWZCkr3Fi4WdlLY%2BlRiEtyNwjAhbVHpQPga7tMyJdv%2FAw%3D%3D)

[def]: https://github.com/user-attachments/assets/972fc04b-25b8-4684-b2c6-d46af43bd022