# Авторизация аутентифицированных пользователей (на клиентской стороне)

Этот файл описывает процесс авторизации пользователей на основе их статуса аутентификации на клиентской стороне с использованием Thymeleaf. Путем отображения или скрытия элементов в представлении в зависимости от статуса аутентификации пользователя можно контролировать видимость определенных функциональностей или действий.

## Цель

Контролировать видимость элементов, связанных с добавлением и удалением студентов, в зависимости от статуса аутентификации пользователя в представлениях Thymeleaf.

## Шаги

1. **Обновление шаблонов Thymeleaf:**

   Измените шаблоны Thymeleaf для условного отображения элементов в зависимости от статуса аутентификации пользователя.

   ```html
   <!DOCTYPE html>
   <html xmlns:th="http://www.thymeleaf.org">
   <head>
       <title>Управление студентами</title>
   </head>
   <body>
       <h1>Управление студентами</h1>

       <!-- Кнопка Добавить студента -->
       <div th:if="${#authorization.expression('isAuthenticated()')}">
           <a href="/addStudent" class="btn btn-primary">Добавить студента</a>
       </div>

       <!-- Кнопка Удалить студента -->
       <div th:if="${#authorization.expression('isAuthenticated()')}">
           <a href="/removeStudent" class="btn btn-danger">Удалить студента</a>
       </div>

       <!-- Другое содержимое -->
       <div>
           <p>Добро пожаловать в систему управления студентами. Здесь вы можете управлять записями студентов.</p>
       </div>
   </body>
   </html>
   ```

   В этом шаблоне:
   - Используется выражение `th:if="${#authorization.expression('isAuthenticated()')}"`, чтобы условно отображать кнопки "Добавить студента" и "Удалить студента" только если пользователь аутентифицирован.

## Объяснение

- **Диалект безопасности Thymeleaf**: Объект `#authorization` является частью диалекта безопасности Thymeleaf, который интегрирует Spring Security с Thymeleaf.
- **Условное отображение**: Атрибут `th:if` используется для условного отображения или скрытия элементов в зависимости от статуса аутентификации пользователя.

Следуя этим шагам, вы можете контролировать видимость элементов в ваших представлениях Thymeleaf в зависимости от статуса аутентификации пользователя, обеспечивая, что только аутентифицированные пользователи могут видеть и взаимодействовать с определенными функциональностями.

---

# [СЛЕДУЮЩАЯ ЗАДАЧА: Авторизация по ролям](authorize-client-role.md)