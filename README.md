# 🌳 OfficeTree

Веб-приложение для учёта сотрудников офиса: кто в какой команде, какая у него зарплата и кто его менеджер. Браузер работает с REST API, данные хранятся в MongoDB.

![Node.js](https://img.shields.io/badge/Node.js-ESM-339933?style=flat-square&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-4-000000?style=flat-square&logo=express)
![MongoDB](https://img.shields.io/badge/MongoDB-Mongoose-47A248?style=flat-square&logo=mongodb&logoColor=white)
![REST](https://img.shields.io/badge/API-REST-0EA5E9?style=flat-square)

## 🛠 Стек

- **Node.js** (ES-модули) и **Express 4**
- **MongoDB** и **Mongoose 8**: схема, индекс по менеджеру, timestamps
- **dotenv**, **cors**
- Фронтенд: HTML, CSS и `public/js/app.js`

## ✨ Возможности

- добавление, редактирование и удаление сотрудников;
- поиск по ID;
- выборка сотрудников по фамилии менеджера;
- веб-форма для всех операций;
- глобальный обработчик ошибок.

Поля сотрудника: `employeeId`, `surname`, `salary`, `managerSurname`.

## 🔌 API

| Метод | Путь | Назначение |
| --- | --- | --- |
| `GET` | `/api/employees?managerSurname=` | список, фильтр по менеджеру |
| `GET` | `/api/employees/:employeeId` | одна запись |
| `POST` | `/api/employees` | создание |
| `PUT` | `/api/employees/:employeeId` | обновление |
| `DELETE` | `/api/employees/:employeeId` | удаление |

## 🚀 Запуск

Нужны **Node.js 18+** и запущенный **MongoDB**.

```bash
cd вяп7
npm install
npm start
```
