# OfficeTree

```markdown
OfficeTree — клиент-серверный каталог сотрудников офиса

Веб-приложение для учёта сотрудников: кто в какой команде, какая зарплата, кто менеджер. Браузер говорит с REST API, данные живут в MongoDB. Подходит как учебный, но цельный fullstack-пример: модель, модули CRUD, роуты, статический фронт.

Стек технологий

![Node.js](https://img.shields.io/badge/Node.js-ESM-339933?logo=nodedotjs)
![Express](https://img.shields.io/badge/Express-4-black?logo=express)
![MongoDB](https://img.shields.io/badge/MongoDB-Mongoose-47A248?logo=mongodb)
![HTML](https://img.shields.io/badge/HTML%20%2B%20CSS-frontend-e34f26)
![REST](https://img.shields.io/badge/API-REST-0ea5e9)

- **Node.js** (ES-модули), **Express 4**
- **MongoDB** + **Mongoose 8** (схема, индекс по менеджеру, timestamps)
- **dotenv**, **cors**
- Статический фронт: HTML, CSS, `public/js/app.js`

Ключевой функционал

REST API `/api/employees`:

| Метод | Путь | Назначение |
| --- | --- | --- |
| `GET` | `/api/employees?managerSurname=` | список, фильтр по менеджеру |
| `GET` | `/api/employees/:employeeId` | одна запись |
| `POST` | `/api/employees` | создание |
| `PUT` | `/api/employees/:employeeId` | обновление |
| `DELETE` | `/api/employees/:employeeId` | удаление |

- Поля сотрудника: `employeeId`, `surname`, `salary`, `managerSurname`.
- Бизнес-логика разнесена по модулям (`addEmployee`, `updateEmployee`, `deleteEmployee`, `getEmployeeById`, `listEmployeesByManager`).
- Веб-форма: добавление, выборка по менеджеру, поиск по ID, правка и удаление.
- Глобальный обработчик ошибок Express.

## Быстрый запуск

Нужны **Node.js 18+** и запущенный **MongoDB**.

```bash
cd вяп7
npm install
