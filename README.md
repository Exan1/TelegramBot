# TelegramBot<br />
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
##Создание и работа телеграм бота:<br />
###[Создание бота](settings/bot_create.py) <br />
###[Получение токена](settings/data.py)<br />
1.Запускаем бота с использованием токена.<br />
2.С помощью Dispatcher поддерживаем работу бота.<br />
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
##Работа телеграм бота<br />
###[В данном файле находится код, который: A. Принимает входящий аудио файл. B.Преобразовывает его в текст. C. Выдает ответ на полученный текст, с помощью добавленной модели логистической регрессии. ](settings/bot_settings.py)<br />
1.С помощью методаv Voice_message_handler принимает входящий аудио файл.<br />
2.C помощью метода audio_to_text из [файла](settings/stt.py) преобразовывает аудио файл в текст.<br />
3.С помощью метода clean_str обрабатывает текст и приводит к нужному виду.<br />
4.В переменнной clf создается экземляр модели логистической регрессии.<br />
5. В переменные X_text и y загружаются данные для обучения из датасета, и после векторизируются для обучения модели.<br />
6. После обучения готовая модель используется для получения ответа на текст, который мы получили из аудио сообщения.<br />
###[Данные, на которых обучается модель логистической регрессии](dialogues.txt)<br />
Датасет состоит из пар вопрос/ответ.<br />
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
##[Методы, которые конвертируют аудио файл из формата wav в текст.](settings/stt.py)<br />
