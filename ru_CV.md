**Сергей Иванов**  
**Go-разработчик**  
Беларусь (открыт к гибридной/офисной работе в Беларуси, удалённой или релокации)  
ivanov.sergei.dev@gmail.com | [GitHub](https://github.com/s-588) | [LinkedIn](https://www.linkedin.com/in/ivanousiarhiej)

## О себе

Go-разработчик, который реализовал mesh-узел маршрутизации в стиле AODV с поддержкой нескольких интерфейсов (userspace UDP), полноценный UDP/TCP DNS-сервер с PostgreSQL, protobuf HTTP API, JWT+RBAC и Prometheus, а также type-safe систему управления транспортом. Ищу позицию стажёра или junior Go backend-разработчика (API, сервисы или инфраструктура). Готов приступить немедленно.

## Навыки

- **Языки**: Go, SQL  
- **Backend и API**: REST, protobuf, gRPC, JWT, Prometheus  
- **Базы данных**: PostgreSQL, sqlc, Goose  
- **Тестирование**: Testcontainers, testify  
- **Сети**: UDP, TCP, DNS, WebSockets  
- **Другое**: Docker Compose, Templ, HTMX
- **Языки (разговорные)**: английский (B2), русский (родной)

## Проекты

### AODV Mesh Node  
**Go | UDP | Bubble Tea | Docker Compose** | [GitHub](https://github.com/s-588/mesh-network)

- Реализовал on-demand mesh-узел маршрутизации в стиле AODV (RREQ, RREP, RERR, HELLO), работающий в userspace поверх UDP/IP с поддержкой нескольких интерфейсов.
- Построил интерактивный TUI на Bubble Tea и CLI, которые общаются с локальным HTTP IPC-сервером и позволяют операторам просматривать соседей/маршруты и отправлять сообщения.
- Создал готовую к запуску топологию из 11 узлов на Docker Compose, охватывающую четыре сети, для end-to-end тестирования протокола без физического оборудования.

### DNS Server  
**Go | PostgreSQL | chi | sqlc | protobuf | Prometheus** | [GitHub](https://github.com/s-588/dns-server)

- Реализовал DNS-сервер, отвечающий на UDP- и TCP-запросы, используя ресурсные записи, хранящиеся в PostgreSQL.
- Сделал полный protobuf HTTP CRUD API с JWT cookie-аутентификацией и RBAC (admin/user); миграции на Goose.
- Добавил метрики Prometheus (латентность запросов, результаты логина, операции с записями) и стриминг JSON-логов в реальном времени по WebSocket.
- Построил CLI и TUI на Bubble Tea, чтобы операторы могли управлять записями и смотреть живые логи без прямого доступа к базе.
- Написал unit-тесты HTTP-хендлеров с testify, mockery и httptest, а также интеграционные тесты слоя репозитория с Testcontainers.

### Transport Management System  
**Go | PostgreSQL | sqlc | Templ | HTMX** | [GitHub](https://github.com/s-588/tms)

- Построил систему управления транспортными заказами для транспортных средств, клиентов, сотрудников и заказов с end-to-end type safety на sqlc и Templ.
- Реализовал динамическое ценообразование заказов на основе расчётов расстояния PostGIS, веса, расхода топлива и скидок за лояльность клиента.
- Добавил интеграционные тесты с Testcontainers, покрывающие CRUD-операции и логику базы данных.
- Реализовал soft-delete и полное аудит-логирование через триггеры базы данных на каждой таблице; генерировал договоры и Excel-отчёты из шаблонов для завершённых заказов.
- Добавил gRPC API параллельно с основным веб-UI на HTTP/Templ + HTMX. Упаковал весь стек в Docker Compose и Taskfile.

## Образование

**Гомельский государственный аграрно-экономический колледж**  
Специальность: Программное обеспечение информационных технологий  
Квалификация: Техник-программист
