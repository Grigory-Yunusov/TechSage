# Контактний список

Програма для управління контактами з можливістю додавання, редагування та видалення інформації про контакти, а також для роботи з нотатками та довідником.

## Список контактів

- **add_name**: Додає ім'я нового контакта.
    ```bash 
    add_name
    Введіть: <Імя>: 'Name'
    ```
- **add_phone**: Додає телефон контакта.
    ```bash 
    add_phone 'Name'
    Введіть номер телефону: 10 цифр: '013456789'
    ```
- **add_birthday**: Додає день народження контакта.
	```bash 
    add_birthday 'Name'
    Введіть дату дня народження у форматі РРРР-ММ-ДД: '2000-12-22'
    ```
- **add_email**: Додає e-mail контакта.
	```bash 
    add_email 'Name'
    Введіть email: 'mail@mail.com'
    ```
- **add_address**: Додає адресу контакта.
	```bash 
    add_email 'Name'
    Введіть адрес: 'Ukraine Kyiv str.Lobanovskogo 2'
    ```
- **list_book**: Повертає список всіх контактів.
	```bash 
    list_book
	┏━━━━━━━━┳━━━━━━━━━━━━┳━━━━━━━━━━━━━┳━━━━━━━━━━━━━━━┳━━━━━━━━━━━━━┓
	┃ Name   ┃ Phone      ┃ Address     ┃ Email         ┃ Birthdays   ┃
	┡━━━━━━━━╇━━━━━━━━━━━━╇━━━━━━━━━━━━━╇━━━━━━━━━━━━━━━╇━━━━━━━━━━━━━┩
	│ Name   │ 0123456789 │ Ukraine Kyiv│ mail@mail.com │ 2000-12-22  │
	└────────┴────────────┴─────────────┴───────────────┴─────────────┘
    ```
- **find_info**: Повертає інформацію за іменем контакта.
	```bash 
    find_info 'Name'
    Name, 0123456789, Ukraine Kyiv│ mail@mail.com │ 2000-12-22
    ```
## Робота з нотатками

- **add_note**: Створює нотатку за Ім'ям користувача.
	```bash 
    add_note 'Name'
    Введіть нотатку: 'Записуєм першу нотатку нашого користувача'
	Введіть теги: '1 нотатка'
    ```
- **edit_note**: Редагує існуючу нотатку.
	```bash 
    edit_note 'Name'
    Введіть нову нотатку: 'Записуєм другу нотатку нашого користувача'
	Введіть теги: '2 нотатка'
    ```
- **find_note**: Відображає нотатки користувача.
	```bash 
    find_note 'Name'
    'Name: Записуєм другу нотатку нашого користувача [Tags: 2 нотатка]'
    ```
- **list_note**: Відображає нотатки користувача.
	```bash 
    list_note 'Name'
    Picture
    [![alt text](https://github.com/Grigory-Yunusov/TechSage/blob/feature/add-address/big_table.png?raw=true)](https://private-user-images.githubusercontent.com/95983273/292049318-a3e8f4a5-2c80-4f4a-9c94-b3a980075914.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTEiLCJleHAiOjE3MDMxMTY3NjgsIm5iZiI6MTcwMzExNjQ2OCwicGF0aCI6Ii85NTk4MzI3My8yOTIwNDkzMTgtYTNlOGY0YTUtMmM4MC00ZjRhLTljOTQtYjNhOTgwMDc1OTE0LnBuZz9YLUFtei1BbGdvcml0aG09QVdTNC1ITUFDLVNIQTI1NiZYLUFtei1DcmVkZW50aWFsPUFLSUFJV05KWUFYNENTVkVINTNBJTJGMjAyMzEyMjAlMkZ1cy1lYXN0LTElMkZzMyUyRmF3czRfcmVxdWVzdCZYLUFtei1EYXRlPTIwMjMxMjIwVDIzNTQyOFomWC1BbXotRXhwaXJlcz0zMDAmWC1BbXotU2lnbmF0dXJlPTRkNDcwZTcwNmMzNjJjN2EzMTJjNGY2OTRjYzZhMDdjNzIwOGIzMzJlODBkZDA4NTFiYjE3NWVlNjI5NjIzYTQmWC1BbXotU2lnbmVkSGVhZGVycz1ob3N0JmFjdG9yX2lkPTAma2V5X2lkPTAmcmVwb19pZD0wIn0.4t-oHIhsLKtmZIL1_TznljS5FY4RRXFGeb15uTwAaOw)


- **delete_all_notes**: Видаляє всі нотатки користувача.
	```bash 
    delete_all_notes 'Name'
    'Усі нотатки для Name було видалено.'
    ```

## Робота з довідником

- **help**: Виклик довідника команд.
	```bash 
    help
    КАРТИНКА НАШОЇ ТАБЛИЦІ
    ```
- **save**: Зберігає зміни що відбулися в довіднику у файл на диску.
	```bash 
    save
    Адресна книга збережена!
    ```
- **load**: Завантаження довідника з файла на диску. Зміни що не були збережені будуть втрачені.
	```bash 
    load
    Адресна книга відновлена
    ```
- **exit**: Вихід із програми, із автоматичним записом змін у файл.
	```bash 
    Good bye!
    ```
## Додаткові функції 

- **days_to_birthday**: Повертає кількість днів до дня народження.
	```bash 
    days_to_birthday
    'До дня народження Name 2000-12-22 залишилось 2 днів'
    ```
- **when**: Повертає список контактів, в яких будуть дні народження у вказаний період.
	```bash 
    when '10'
    'До дня народження Name 2000-12-22 залишилось 2 днів'
    ```
- **sort_files**: Сортує файли у вказаному каталозі.

**Приклад використання:**

Програма реалізую роботую з Книгою контактів Робота відбувається в декількох напрямках
    '''Телефонна книга:'''
