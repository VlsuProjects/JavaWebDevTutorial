# Настройка Thymeleaf с Spring Security

## Цель
Цель этого задания - интегрировать Thymeleaf с Spring Security, обеспечивая использование дополнительных диалектов и утилит, предоставляемых библиотекой `thymeleaf-extras-springsecurity6`.

## Шаги

1. **Gradle (Groovy):**

   Добавьте зависимость `thymeleaf-extras-springsecurity6` в ваш файл `build.gradle`:

   ```groovy
   implementation 'org.thymeleaf.extras:thymeleaf-extras-springsecurity6:3.0.4.RELEASE'
   ```

2. **Maven:**

   Добавьте следующую зависимость в ваш файл `pom.xml`:

   ```xml
   <dependency>
       <groupId>org.thymeleaf.extras</groupId>
       <artifactId>thymeleaf-extras-springsecurity6</artifactId>
       <version>3.0.4.RELEASE</version>
   </dependency>
   ```

---

# [СЛЕДУЮЩЕЕ ЗАДАНИЕ: Создать базовую реализацию для пользователя](base-implementation-user.md)
