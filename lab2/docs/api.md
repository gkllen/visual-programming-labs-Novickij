# Документация REST API (Node-RED)

**Автор:** Novickij  
**Лабораторная работа:** №2  
**Базовый URL:** `http://localhost:1880`

---

## 1. GET /api/text

Возвращает простой текстовый ответ (`text/plain`).

* **Метод:** `GET`
* **URL:** `/api/text`
* **Код ответа:** `200 OK`
* **Тело ответа:**
```text
Hello from Node-RED API! Author: Novickij
2. GET /api/info
Возвращает системную информацию и данные автора в формате JSON.

Метод: GET

URL: /api/info

Заголовки ответа: Content-Type: application/json

Код ответа: 200 OK

Тело ответа:

JSON
{
  "status": "success",
  "student": "Novickij",
  "lab": 2,
  "environment": "Node-RED on Docker"
}
3. GET /api/items
Возвращает список компонентов системы при передаче обязательного параметра или ошибку валидации при его отсутствии.

Метод: GET

URL: /api/items

Query-параметры:

type (строка, обязательный). Ожидаемое значение: all.

Успешный запрос (200 OK)
Запрос: GET /api/items?type=all

Тело ответа:

JSON
[
  { "id": 1, "name": "Node-RED Service", "status": "active" },
  { "id": 2, "name": "Mosquitto Broker", "status": "active" },
  { "id": 3, "name": "Lab Documentation", "status": "ready" }
]
Ошибка валидации (400 Bad Request)
Запрос: GET /api/items

Тело ответа:

JSON
{
  "error": "Bad Request",
  "message": "Missing or invalid 'type' query parameter. Use ?type=all"
}