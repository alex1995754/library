# Library Project

Проект представляет собой онлайн-книжный магазин с функциональностью корзины и оформления заказов. В проекте используется Flask для сервера и SQLite для хранения данных о книгах.

## Структура проекта

library/ │ 

├── app.py # Логика программы и сервер Flask 

├── books.db # База данных с книгами 

├── create_db.py # Скрипт для создания базы данных 

├── run_all.py # Скрипт для запуска сервера и проверки зависимостей 

├── start_server.bat # Скрипт для запуска сервера на Windows 

├── bookstore.html # Главная страница без запуска сервера 


├── templates/ # Папка с HTML-шаблонами │ 

├── index.html # Главная страница

├── search_results.html # Страница с результатами поиска

├── cart.html # Страница с корзиной

├── checkout.html # Страница оформления заказа

└── checkout_success.html # Страница с сообщением об успешном заказе


├── static/ # Папка с статичными файлами │ 

├── css/ # Папка с файлами стилей │ │ 

└── styles.css # Стили проекта

└── images/ # Папка с изображениями │ │

└── book.jpg # Изображение книги

## Установка

### 1. Распаковка проекта

1. Распакуйте архив проекта `library-main` в удобную директорию.

### 2. Запуск с использованием `run_all.py`

Для удобства можно запустить проект через файл `run_all.py`, который:
- Проверяет наличие необходимых зависимостей (Flask и sqlite3).
- Устанавливает недостающие модули, если они не установлены.
- Запускает сервер Flask.
- Открывает главную страницу в браузере.

**Как запустить**:
1. Откройте терминал или командную строку.
2. Перейдите в корневую директорию проекта.
3. Выполните команду:

    ```bash
    python run_all.py
    ```

### 3. Запуск вручную

Если вы не хотите использовать `run_all.py`, можете выполнить следующие шаги:

#### Запуск сервера вручную:

1. Для **Windows**: Запустите файл `start_server.bat`, чтобы запустить сервер Flask.
2. Для **Linux/macOS**: Запустите сервер с помощью команды:

    ```bash
    python app.py
    ```

#### Открытие главной страницы:

- Откройте файл `bookstore.html` в браузере для просмотра главной страницы без запуска сервера.

## Описание страниц

1. **Главная страница (`index.html`)**:
   - Показывает случайные книги.
   - Включает форму для поиска книг по названию или автору.

2. **Результаты поиска (`search_results.html`)**:
   - Показывает список книг, соответствующих запросу пользователя.

3. **Корзина (`cart.html`)**:
   - Показывает список книг, добавленных в корзину пользователем.
   - Отображает количество каждой книги в корзине.

4. **Оформление заказа (`checkout.html`)**:
   - Позволяет пользователю оформить заказ.
   - Показывает список книг в корзине с количеством.

5. **Успешное оформление заказа (`checkout_success.html`)**:
   - Страница, отображающая сообщение об успешном заказе после его подтверждения.

## Структура базы данных

База данных `books.db` содержит таблицу `books` с следующими полями:

- `id`: Уникальный идентификатор книги.
- `title`: Название книги.
- `author`: Автор книги.
- `amount`: Количество доступных экземпляров книги в магазине.