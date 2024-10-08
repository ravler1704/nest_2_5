# Домашнее задание к занятию «2.5. Валидация и обработка ошибок. Interceptors, pipes»

**Правила выполнения домашней работы.**
* Выполняйте домашнее задание в отдельной ветке проекта на GitHub.
* В поле для сдачи работы прикрепите ссылку на ваш проект в Git.
* На проверку можно отправить как все задачи вместе, так и каждую задачу по отдельности.
* Во время проверки вашей домашней работы по частям будет стоять статус «На доработке».
* Любые вопросы по решению задач можете задавать в чате учебной группы.

**Выполните задания.**

**Задание 1.**

Создать Interceptor и подключить его в локальной или глобальной области видимости для перехвата и обработки исключений.
Interceptor должен оборачивать результат при успешном запросе в структуру:
````
{
    status: "success",
    data: ... // данные из контроллера
}
````
При запросе с ошибкой оборачивать в структуру:
````
{
    status: "fail",
    data: ... // сведения об ошибке
}
````
**Задание 2.**

Создать Pipe и подключить его в локальной или глобальной области видимости для валидации данных в body, params или query запроса, используя соответствующие декораторы (@Body, @Query, @Params).

**Задание 3.**

Создать метод валидации данных входящего запроса в Pipe с использованием библиотеки Joi или class-validator и DTO.

**Задание 4.**

Создать Exception Filter и подключить его в локальной или глобальной области видимости для перехвата и формирования унифицированных сообщений об исключениях.
Сообщение должно иметь формат:
````
{
    timestamp: ..., // дата и время
    status: "fail",
    data: ..., // сведения об ошибке
    code: ..., // код ошибки при наличии в объекте ошибки. В случае отсутствия, по умолчанию code = 500
}
````
