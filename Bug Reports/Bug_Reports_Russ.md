# Отчет об ошибке N1

## Восстановление пароля – Процесс отправки ссылки на электронную почту

## Environment

| Parameter | Details |
|---|---|
| Test Device | Laptop, VivoBook_ASUSLaptop X509JB_X509JB |
| Operating System | Microsoft Windows 11 Pro Version 10.0.26100 Build 26100 |
| Browser | Google Chrome Version 133.0.6943.127 (Official Build) (64-bit) |
| Reproducibility Rate | 100% |

## Test Data

| Email Address |
|---|---|
| testUser@gmail.com |

## Precondition
- Пользователь зарегистрирован в системе
- Пользователь не авторизован в системе

## Steps to Reproduce

| **N** | **Steps** | **Test Data** |
|---|---|---|
| 1 | Откройте веб-сайт https://.....ge/ka/ | - |
| 2 | Нажмите кнопку **«Авторизация»** в хедере | - |
| 3 | Нажмите кнопку **«Забыли пароль?»** под полем ввода пароля | - |
| 4 | Введите зарегистрированный адрес электронной почты | testUser@gmail.com |
| 5 | Нажмите кнопку **«Отправить ссылку для сброса пароля»** | - |

## Actual Result
Ссылка для сброса пароля не отправляется на электронную почту, появляется сообщение об ошибке:

> “An error occurred while sending the email.”

## Expected Result
Ссылка для сброса пароля успешно отправляется, и появляется сообщение:

> “Password reset email has been sent successfully.”

## Attachment
Example

# Отчет об ошибке N2

## Logout & Re-login: Некорректная работа корзины и списка желаемого после выхода со страницы Checkout и повторного входа

## Environment

| Parameter | Details |
|---|---|
| Test Device | Laptop, VivoBook_ASUSLaptop X509JB_X509JB |
| Operating System | Microsoft Windows 11 Pro Version 10.0.26100 Build 26100 |
| Browser | Google Chrome Version 133.0.6943.127 (Official Build) (64-bit) |
| Reproducibility Rate | 100% |

## Test Data

| Credentials |
|---|---|
| Email: testUser2@gmail.com |
| Password: Test123! |

## Precondition
- Пользователь авторизован в системе.
- В корзине находится как минимум один товар.
- В списке желаемого находится как минимум один товар.

## Steps to Reproduce

| **N** | **Steps** | **Test Data** |
|---|---|---|
| 1 | Откройте веб-сайт https://......ge/ka/ | - |
| 2 | Нажмите кнопку **«Корзина»** в хедере | - |
| 3 | Нажмите кнопку **«Оформить заказ»** | - |
| 4 | На странице с логотипом нажмите кнопку с инициалами профиля (T U) | - |
| 5 | В выпадающем меню нажмите кнопку **«Выйти»** | - |
| 6 | Повторно войдите в систему под той же учетной записью | Email Address |

## Actual Result
- После выхода из системы корзина и список желаемого не очищаются.
- После повторного входа корзина становится пустой, а список желаемого остается без изменений.

## Expected Result
- При выходе из системы должны очищаться как корзина, так и список желаемого.
- После повторного входа в систему в корзине и списке желаемого должны отображаться и сохраняться те же товары и их количество, которые были у пользователя до выхода из системы.

## Attachment
Example

# Отчет об ошибке N3

## Dropdown: На странице «Вакансии» категория «Horeca» дублируется в выпадающем списке категорий и после обновления страницы заменяется другой категорией

## Environment

| Parameter | Details |
|---|---|
| Test Device | Laptop, VivoBook_ASUSLaptop X509JB_X509JB |
| Operating System | Microsoft Windows 11 Pro Version 10.0.26100 Build 26100 |
| Browser | Google Chrome Version 133.0.6943.127 (Official Build) (64-bit) |
| Reproducibility Rate | 100% |

## Steps to Reproduce

| **N** | **Steps** | **Test Data** |
|---|---|---|
| 1 | Откройте веб-сайт https://......ge/ka/ | - |
| 2 | Нажмите кнопку **«Вакансии»** в навбаре | - |
| 3 | В панели фильтров нажмите кнопку **«Категория»** | - |
| 4 | Обновите страницу | - |

## Actual Result
- В выпадающем меню категория **«Horeca»** изначально отображается дважды.
- После обновления страницы второй пункт **«Horeca»** заменяется категорией **«Гостеприимство»**.

## Expected Result
- Каждая категория должна отображаться в выпадающем меню только один раз и не должна изменяться после обновления страницы.

## Attachment
Example

# Отчет об ошибке N4

## Filters: Иконки цветов не соответствуют своим названиям в фильтре цветов

## Environment

| Parameter | Details |
|---|---|
| Test Device | Laptop, VivoBook_ASUSLaptop X509JB_X509JB |
| Operating System | Microsoft Windows 11 Pro Version 10.0.26100 Build 26100 |
| Browser | Google Chrome Version 133.0.6943.127 (Official Build) (64-bit) |
| Reproducibility Rate | 100% |

## Precondition
- Открыт каталог категории **“Мужчины”**
- В системе присутствуют товары разных цветов

## Steps to Reproduce

| **N** | **Steps** | **Test Data** |
|---|---|---|
| 1 | Откройте веб-сайт https://......ge/ka/ | - |
| 2 | Прокрутите страницу до секции фильтра цветов | - |

## Actual Result
- В фильтре цветов для названий **Розовый, Бежевый, Темно-синий, Зеленый, Серый, Золотой, Черно-белый, Желтый, Голубой** отображаются некорректные цветовые иконки.
- По умолчанию отображается белая иконка.

## Expected Result
- Для каждого названия цвета в фильтре должна отображаться соответствующая цветовая иконка.

## Attachment
Example
