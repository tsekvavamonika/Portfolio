# Bug Report N1

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

# Bug Report N2

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

# Bug Report N3

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

# Bug Report N4

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

# Bug Report N5

## Authentication: Пользователь остается авторизованным после выхода из системы и обновления страницы

## Environment

| Parameter | Details |
|---|---|
| Test Device | Laptop, VivoBook_ASUSLaptop X509JB_X509JB |
| Operating System | Microsoft Windows 11 Pro Version 10.0.26100 Build 26100 |
| Browser | Google Chrome Version 133.0.6943.127 (Official Build) (64-bit) |
| Reproducibility Rate | 100% |

## Precondition
- Пользователь авторизован в системе
- В аккаунте пользователя есть сохраненные товары в корзине

## Steps to Reproduce

| **N** | **Steps** | **Test Data** |
|---|---|---|
| 1 | Откройте веб-сайт https://......ge/ka/ | - |
| 2 | Войдите в систему с помощью валидной учетной записи | testUser@gmail.com |
| 3 | Нажмите на иконку профиля | - |
| 4 | Нажмите кнопку **«Logout»** | - |
| 5 | Обновите страницу | - |
| 6 | Попробуйте открыть страницу профиля напрямую | - |

## Actual Result
- После обновления страницы пользователь остается частично авторизованным.
- Страница профиля остается доступной без повторного входа.

## Expected Result
- После выхода из системы сессия должна полностью завершаться.
- Защищенные страницы не должны быть доступны после logout.

## Attachment
Example

# Bug Report N6

## Payment: После успешной оплаты статус заказа остается “Pending”

## Environment

| Parameter | Details |
|---|---|
| Test Device | Laptop, VivoBook_ASUSLaptop X509JB_X509JB |
| Operating System | Microsoft Windows 11 Pro Version 10.0.26100 Build 26100 |
| Browser | Google Chrome Version 133.0.6943.127 (Official Build) (64-bit) |
| Reproducibility Rate | 100% |

## Precondition
- В корзине пользователя есть товары

## Steps to Reproduce

| **N** | **Steps** | **Test Data** |
|---|---|---|
| 1 | Перейдите к оформлению заказа | - |
| 2 | Выполните оплату с помощью валидной банковской карты | Test Visa Card |
| 3 | Откройте историю заказов | - |

## Actual Result
- Оплата проходит успешно, но статус заказа остается **“Pending”**.

## Expected Result
- После успешной оплаты статус заказа должен измениться на **“Paid”** или **“Confirmed”**.

## Attachment
Example

# Bug Report N7

## Cart: Дублирование товаров после двойного нажатия кнопки “Add to Cart”

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
| 1 | Откройте страницу товара | - |
| 2 | Быстро дважды нажмите кнопку **“Add to Cart”** | - |
| 3 | Откройте корзину | - |

## Actual Result
- В корзину добавляются дублирующиеся товары.

## Expected Result
- Независимо от количества быстрых нажатий товар должен добавляться только один раз.

## Attachment
Example

# Bug Report N8

## Authorization: Неавторизованный пользователь может открыть страницу Checkout

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
| 1 | Выйдите из системы | - |
| 2 | Вставьте прямую ссылку checkout в браузер | /checkout |
| 3 | Нажмите Enter | - |

## Actual Result
- Неавторизованный пользователь может получить доступ к странице checkout.

## Expected Result
- Неавторизованный пользователь должен быть перенаправлен на страницу логина.

## Attachment
Example

# Bug Report N9

## Product Page: Товар с нулевым остатком все еще доступен для покупки

## Environment

| Parameter | Details |
|---|---|
| Test Device | Laptop, VivoBook_ASUSLaptop X509JB_X509JB |
| Operating System | Microsoft Windows 11 Pro Version 10.0.26100 Build 26100 |
| Browser | Google Chrome Version 133.0.6943.127 (Official Build) (64-bit) |
| Reproducibility Rate | 100% |

## Precondition
- Количество товара на складе равно 0

## Steps to Reproduce

| **N** | **Steps** | **Test Data** |
|---|---|---|
| 1 | Откройте страницу товара с нулевым остатком | - |
| 2 | Нажмите кнопку **“Add to Cart”** | - |
| 3 | Перейдите к оформлению заказа | - |

## Actual Result
- Товар с нулевым остатком успешно добавляется в корзину и доступен для покупки.

## Expected Result
- Товары с нулевым остатком не должны быть доступны для покупки.

## Attachment
Example

# Bug Report N10

## Checkout: Общая сумма заказа изменяется после обновления страницы

## Environment

| Parameter | Details |
|---|---|
| Test Device | Laptop, VivoBook_ASUSLaptop X509JB_X509JB |
| Operating System | Microsoft Windows 11 Pro Version 10.0.26100 Build 26100 |
| Browser | Google Chrome Version 133.0.6943.127 (Official Build) (64-bit) |
| Reproducibility Rate | 100% |

## Precondition
- Пользователь авторизован
- В корзине находится несколько товаров

## Steps to Reproduce

| **N** | **Steps** | **Test Data** |
|---|---|---|
| 1 | Откройте веб-сайт https://......ge/ka/ | - |
| 2 | Добавьте несколько товаров в корзину | - |
| 3 | Перейдите к оформлению заказа | - |
| 4 | Обратите внимание на общую сумму заказа | - |
| 5 | Обновите страницу checkout | - |

## Actual Result
- После обновления страницы общая сумма заказа изменяется.
- Расчет скидки становится некорректным.

## Expected Result
- Общая сумма заказа и скидка должны оставаться неизменными после обновления страницы.

## Attachment
Example

# Bug Report N11

## Session Timeout: Пользователь может выполнять действия после истечения сессии

## Environment

| Parameter | Details |
|---|---|
| Test Device | Laptop, VivoBook_ASUSLaptop X509JB_X509JB |
| Operating System | Microsoft Windows 11 Pro Version 10.0.26100 Build 26100 |
| Browser | Google Chrome Version 133.0.6943.127 (Official Build) (64-bit) |
| Reproducibility Rate | 100% |

## Precondition
- Пользователь авторизован

## Steps to Reproduce

| **N** | **Steps** | **Test Data** |
|---|---|---|
| 1 | Войдите в систему | testUser@gmail.com |
| 2 | Не выполняйте никаких действий до истечения времени сессии | - |
| 3 | Попробуйте добавить товар в корзину | - |

## Actual Result
- Пользователь все еще может выполнять действия после истечения сессии.

## Expected Result
- После истечения сессии пользователь должен быть перенаправлен на страницу логина.

## Attachment
Example
