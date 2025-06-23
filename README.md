# ⚖️ Clairvoyant – AI-Powered Contract Assistant

**Clairvoyant** is an AI-driven tool that helps users analyze contracts, extract key clauses, and manage legal deadlines effortlessly. Built on top of the [`oseughu/svelte-starter-kit`](https://github.com/oseughu/svelte-starter-kit), it combines the flexibility of Laravel with the simplicity and power of modern Svelte.

---

## 📦 Tech Stack

| Layer         | Stack & Tools                             |
|---------------|--------------------------------------------|
| **Frontend**  | Svelte 5, Inertia.js, Vite, Tailwind CSS, Shadcn/ui |
| **Backend**   | Laravel 11 (API routes + controllers)      |
| **AI Layer**  | OpenAI API (via Laravel backend)           |
| **Storage**   | Laravel File Storage (for contracts)       |
| **State**     | Svelte Stores                              |
| **Routing**   | Laravel Routes (via Inertia)               |

---

## 🎯 Project Goals

- ✅ Upload contracts (PDF, DOCX)
- ✅ Analyze content via AI (OpenAI or LangChain)
- ✅ Extract and highlight clauses (e.g. Termination, Auto-renewal)
- ✅ Generate deadline-based reminders
- ✅ Provide users with simple insights into risks or obligations

---

## ✨ Features (MVP Phase)

### Upload & Analyze
- File upload UI (drag-and-drop)
- Backend parses and stores file
- Calls AI to summarize and return clause structure

### Clause Breakdown
- Display key clauses with color-coded risk levels
- Group clauses by type (e.g. Financial, Termination, Confidentiality)

### Smart Reminders
- Identify key contract dates (renewals, expirations)
- Display as upcoming alerts in a timeline or dashboard

---

## 📁 Project Structure Overview

```
clairvoyant/
├── resources/
│   └── js/               → Svelte 5 frontend
│       ├── Pages/
│       ├── Components/
│       └── stores/
├── routes/
│   └── web.php          → Laravel routes via Inertia
│   └── api.php          → JSON API for AI & storage
├── app/Http/Controllers/
│   └── ContractController.php
│   └── AIController.php
├── storage/app/contracts/ → Uploaded files
```

---

## 🧪 API Endpoints (Planned)

| Method | Route             | Purpose                          |
|--------|-------------------|----------------------------------|
| POST   | `/api/upload`     | Handle file upload               |
| POST   | `/api/analyze`    | Call OpenAI and parse response   |
| GET    | `/api/reminders`  | Return upcoming dates from text  |

---

## 🔐 Auth & Security

- Auth planned via Laravel Sanctum (for multi-user mode)
- Basic input sanitization and file validation included

---

## 🚧 Status

This project is under active development:
- [x] Laravel + Svelte starter setup complete
- [ ] Custom UI components added
- [ ] File upload to Laravel storage
- [ ] AI integration via OpenAI
- [ ] Reminder system built from clause metadata

---

## 👤 About the Developer

Hi, I’m **Andrei Zidariu**, a full-stack developer focused on building thoughtful tools with modern frameworks and purposeful AI integrations.

Other projects in this series:
- 🧭 Pathfinder – Mental clarity and wellbeing tracker
- 🧠 Second Brain AI – Config-aware assistant for developers

---

## 📄 License

MIT – Free for personal and commercial use.
