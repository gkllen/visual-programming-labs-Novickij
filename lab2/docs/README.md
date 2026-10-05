# Лабораторная работа №2

**Студент:** Novickij  
**Курс:** Визуальное программирование  
**Среда:** Docker (`mynodered`), Node-RED v5.0.7, Node.js v24.20.0  

---

## 1. Проверка окружения

Контейнер Node-RED развёрнут и запущен в Docker. Версии ПО подтверждены через логи контейнера.

![Проверка версий Docker и Node-RED](screenshots/00-docker-version.png)

---

## 2. Реализованные потоки (Node-RED Flows)

Ниже представлены скриншоты разработанных узлов и потоков данных:

### 2.1. Базовая отладка и функции
* **Inject & Debug:**
  ![Inject & Debug](screenshots/01-inject-debug.png)

* **Узел Function:**
  ![Function Node](screenshots/02-function.png)

### 2.2. Управление логикой и потоками
* **Узел Switch:**
  ![Switch Node](screenshots/03-switch.png)

* **Узел Change:**
  ![Change Node](screenshots/04-change.png)

* **Узел Template:**
  ![Template Node](screenshots/05-template.png)

### 2.3. Сетевые протоколы и форматы данных
* **HTTP Request:**
  ![HTTP Request](screenshots/06-http-request.png)

* **MQTT Protocol:**
  ![MQTT Protocol](screenshots/07-mqtt.png)

* **Работа с JSON:**
  ![JSON Format](screenshots/08-json.png)

### 2.4. Структурирование и обработка ошибок
* **Подпотоки (Subflow):**
  ![Subflow](screenshots/09-subflow.png)

* **Перехват ошибок (Catch & Status):**
  ![Catch and Status](screenshots/10-catch-status.png)