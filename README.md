# **Проект «API для Yatube»**
---

### **Описание проекта:**
Социальная сеть "Yatube" , в которой можно писать посты , коментировать их , и подписываться на понравившихся авторов.
---

### **Технологии:**
Python 3.7.0 <br>
Django 3.2.16 <br>
Visual Studio Code <br>
Postman
---

### **Как запустить проект:**
Visual Studio Code , терминал bash , директория с проектами (C/Dev/)
- Клонировать проект с GitHub: git clone https://github.com/Aibulat-Ibragimov/api_final_yatube.git
- Перейти в папку проекта: cd api_final_yatube/
- Установить виртуальное окружение: python -m venv venv
- Активариовать виртуальное окружение: source venv/Scripts/activate
- Установить зависимости из файла requirements.txt: pip install -r requirements.txt
- Дополнительно установить: pip install djoser djangorestframework-simplejwt==4.7.2
- Выполнить миграции: python manage.py migrate
- Запустить проект: python manage.py runserver
---

### **Примеры запросов:**
- **GET** http://127.0.0.1:8000/api/v1/posts/{id}/ <br>
<sub>Получить список всех публикаций. При указании параметров limit и offset выдача должна работать с пагинацией.</sub>
```json
{
"id": 0,
"author": "string",
"text": "string",
"pub_date": "2024-01-10T12:18:05Z",
"image": "string",
"group": 0
}
```

- **POST** http://127.0.0.1:8000/api/v1/posts/ <br>
<sub>Добавление новой публикации в коллекцию публикаций. Анонимные запросы запрещены.</sub>
```json
*Создаем пост*
{
"text": "string",
"image": "string",
"group": 0
}
*Пост создался*
{
"id": 0,
"author": "string",
"text": "string",
"pub_date": "2024-01-10T12:18:05Z",
"image": "string",
"group": 0
}
```

- **PUT** http://127.0.0.1:8000/api/v1/posts/{id}/ <br>
<sub>Обновление публикации по id. Обновить публикацию может только автор публикации. Анонимные запросы запрещены.</sub>
```json
*Обновляем пост*
{
"text": "string",
"image": "string",
"group": 0
}
*Обновленный пост*
{
"id": 0,
"author": "string",
"text": "string",
"pub_date": "2024-01-10T12:32:18Z",
"image": "string",
"group": 0
}
```

- **DELETE** http://127.0.0.1:8000/api/v1/posts/{id}/ <br>
<sub>Удаление публикации по id. Удалить публикацию может только автор публикации. Анонимные запросы запрещены.</sub>
```json
*Удалить публикацию может только автор публикации.*
{
"detail": "Учетные данные не были предоставлены."
}
```

---

**~~Автор проекта:~~** Ибрагимов Айбулат https://github.com/Aibulat-Ibragimov
