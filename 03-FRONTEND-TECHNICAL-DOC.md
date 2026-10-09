---

## 📄 File 3: `03-FRONTEND-TECHNICAL-DOC.md` (Tài liệu kỹ thuật Frontend)

```markdown
# Tài Liệu Kỹ Thuật Frontend (Frontend Technical Architecture)
**Công nghệ đề xuất:** React.js (Vite) / Next.js, TailwindCSS, Redux Toolkit / React Query.

---

## 1. Kiến trúc Kiến trúc Thư mục (Project Structure)

```text
src/
├── assets/          # Static assets (images, icons)
├── components/      # Common UI Components (Button, Input, Modal, Badge...)
├── features/        # Business Modules
│   ├── auth/        # Login, Register, Profile
│   ├── restaurant/  # Restaurant detail, Menu, Search
│   ├── cart/        # Cart drawer, Checkout logic
│   └── order/       # Order tracking, History
├── services/        # API calls (Axios instances, endpoints)
├── store/           # Global State Management (Redux/Zustand)
├── routes/          # Router configuration (React Router DOM)
└── utils/           # Helper functions (formatCurrency, formatDate...)