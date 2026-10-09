---

## 📄 File 4: `04-ADMIN-BACKEND-TECHNICAL-DOC.md` (Tài liệu kỹ thuật Backend & Admin)

```markdown
# Tài Liệu Kỹ Thuật Backend & Admin (Backend & Database Architecture)
**Công nghệ đề xuất:** Node.js (Express/NestJS) hoặc PHP (Laravel), MySQL / PostgreSQL, Redis, Socket.io.

---

## 1. Kiến trúc Hệ thống (System Architecture)

```text
[ Client App / Web Admin ] 
          │
          ▼
   [ Nginx Reverse Proxy ]
          │
          ▼
   [ Node.js / Laravel API Gateway ]
     ├── Authentication (JWT)
     ├── RESTful APIs (CRUD Menu, Orders, Users)
     └── WebSocket Server (Real-time updates)
          │
     ┌────┴───────────────┐
     ▼                    ▼
[ MySQL Database ]    [ Redis Cache ]
(Data lưu trữ)       (Session, Order Queue)