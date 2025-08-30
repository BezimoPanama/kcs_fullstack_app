# 🧑‍💻 Fullstack User Management System for KCS

A fullstack monorepo project featuring a complete user management system built with modern TypeScript tools. This project is designed as a production-ready seed, demonstrating enterprise-level architecture, clean code practices, and developer experience best practices.

---

## 📚 Table of Contents

- [🔍 Features](#-features)
- [🛠️ Tech Stack](#️-tech-stack)
  - [Frontend](#frontend)
  - [Backend](#backend)
  - [Dev Tools](#dev-tools)
- [🐳 Local Development Setup](#-local-development-setup)
- [📦 VS Code Extensions for Fullstack TypeScript Development](#-vs-code-extensions-for-fullstack-typescript-development)
  - [🔧 Extensions Installed](#-extensions-installed)
  - [💻 CLI Installation (Optional)](#-cli-installation-optional)

---

## 🔍 Features

- User registration, login, logout
- Profile view and edit (email, phone)
- Password update and account deletion
- Input validation and sanitization
- Scalable monorepo architecture
- Shared types between frontend and backend

---

## 🛠️ Tech Stack

### Frontend

- **Next.js** — React-based framework with full SSR/SSG support
- **TypeScript** — Strong typing across the stack
- **Tailwind CSS** — Utility-first CSS for fast styling
- **shadcn/ui** — Reusable, accessible React components
- **react-hook-form + zod** — Form state + schema validation

### Backend

- **NestJS** — Structured Node.js backend framework using TypeScript
- **PostgreSQL** — Relational database
- **Prisma** _(optional)_ — Type-safe ORM and DB migrations
- **JWT** — Stateless authentication

### Dev Tools

- **pnpm** — Fast monorepo package manager
- **TurboRepo** — Caching and task running in monorepo
- **ESLint & Prettier** — Code linting and formatting
- **DotENV** — Environment variable management
- **GitLens** — Git insights in VS Code

---

## 🐳 Local Development Setup

- Dockerized PostgreSQL database
- Optional Redis for rate limiting or session management
- Dev containers for consistent local environments _(optional)_

---

### ⚙️ Tooling Environment (pnpm + Volta)

This project uses **[pnpm](https://pnpm.io/)** and **[Volta](https://volta.sh/)** to ensure a fast, predictable, and isolated JavaScript toolchain across machines and contributors.

| Tool         | Purpose                                                                                                                                                                                                     |
| ------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 🔹 **pnpm**  | A fast, disk-efficient package manager optimized for monorepos. It uses symlinks instead of deep copies and strictly respects `node_modules` boundaries.                                                    |
| 🔹 **Volta** | A zero-config JavaScript runtime manager that ensures everyone uses the same Node.js, pnpm, and other tool versions per project. It pins versions in `package.json` or `.volta` so no one breaks the stack. |

#### 📥 Install pnpm

Install volta

```bash
curl https://get.volta.sh | bash
```

Install pnpm

```bash
volta install pnpm
```

Install node

```bash
volta install node
```

---

## 📦 VS Code Extensions for Fullstack TypeScript Development

This list includes handpicked extensions for an efficient developer workflow using **Next.js**, **NestJS**, **Tailwind CSS**, **shadcn/ui**, and **PostgreSQL**.

---

### 🔧 Extensions Installed

| Extension Name                         | Purpose                                             |
| -------------------------------------- | --------------------------------------------------- |
| ✅ **Tailwind CSS IntelliSense**       | Autocomplete for Tailwind classes                   |
| ✅ **shadcn UI Snippets** _(optional)_ | Faster UI development with component snippets       |
| ✅ **ESLint**                          | Code linting on save                                |
| ✅ **Prettier**                        | Auto-formatting                                     |
| ✅ **Prisma** _(if using)_             | Highlighting + autocomplete for Prisma schema files |
| ✅ **DotENV**                          | Syntax highlighting for `.env` files                |
| ✅ **GitLens**                         | Enhanced Git history, blame, and insights           |
| ✅ **Path Intellisense**               | Suggests file paths as you type                     |
| ✅ **Turbo Console Log**               | Insert `console.log()` quickly for debugging        |
| ✅ **Error Lens**                      | Shows inline TypeScript and ESLint errors           |

---

### 💻 CLI Installation (Optional)

Install them all at once using the terminal:

```bash
code --install-extension bradlc.vscode-tailwindcss \
     --install-extension phthh.shadcn-ui-snippets \
     --install-extension dbaeumer.vscode-eslint \
     --install-extension esbenp.prettier-vscode \
     --install-extension prisma.prisma \
     --install-extension mikestead.dotenv \
     --install-extension eamodio.gitlens \
     --install-extension christian-kohler.path-intellisense \
     --install-extension ChakrounAnas.turbo-console-log \
     --install-extension usernamehw.errorlens
```

## Structure

user_management/
├── apps/
│ ├── web/ ← frontend (Next.js)
│ └── api/ ← backend (NestJS)
├── packages/
│ ├── ui/ ← shared shadcn components
│ ├── types/ ← shared TypeScript types
│ └── config/ ← shared Tailwind, ESlint, etc.
├── package.json
