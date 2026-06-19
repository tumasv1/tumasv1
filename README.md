## 👤 Михаил Тумасов

**AI Technical / Product Manager · Архитектура LLM-слоя · Управление AI-командами**

12+ лет в IT: системный анализ, управление проектами, руководство командой аналитиков.
Выстраиваю LLM-инфраструктуру и агентские архитектуры — от прототипа до production: шлюзы, RAG-системы, оркестрация агентов, метрики качества.

> 💼 Открыт к предложениям — ищу роль AI Technical Manager / AI Product Manager

---

### 🚀 Чем занимаюсь сейчас

- 🏗️ Строю production LLM-инфраструктуру (шлюз, мультитенантность, бюджеты, fallback)
- 🤖 Разрабатываю агентные RAG-системы на LangGraph
- 📊 Применяю RAGAS и golden sets для оценки качества AI-систем

---

### 🛠️ Навыки

| Область | Уровень |
|---|---|
| 🤖 LLM-агенты (LangGraph, ReAct, tools) | Практический опыт |
| 🔍 RAG-архитектуры (гибридный поиск, чанкинг) | Практический опыт |
| 📊 Оценка качества AI (RAGAS, golden sets) | Практический опыт |
| 🏗️ LLM-инфраструктура (LiteLLM, шлюзы, мультитенантность) | Практический опыт |
| 🐳 Docker, GitHub Actions, CI/CD | Использую в проектах |
| 👥 Управление AI-командами и продуктом | 5 лет опыта |
| 🐍 Python (LangChain, FastAPI, Pydantic) | Активно использую |

---

### 💡 Проекты

**[RAGv2 — Агентный RAG по базе знаний Obsidian](https://github.com/tumasv1/RAGv2-Agentic-RAG)**

Персональный ИИ-ассистент поверх Obsidian vault. CPU-only, production deployment на домашнем сервере.

- 🧠 LangGraph ReAct-агент + гибридный поиск (dense + BM25 + RRF)
- 📦 Parent-Child чанкинг, RAGAS-оценка (18 golden cases), 12 ADR
- ⚙️ FastAPI + PWA, Docker Compose, GitHub Actions CI/CD

---

**[LLM-gateway — Единый шлюз ко всем LLM-моделям](https://github.com/tumasv1/LLM-gateway)**

Production-инфраструктура на LiteLLM Proxy для управления всеми AI-инструментами из одной точки.

- 🔀 Балансировка нагрузки между провайдерами (OpenRouter, nano-gpt) + автоматический fallback
- 💰 Мультитенантность: virtual keys с бюджетами, лимитами rpm/tpm и списком разрешённых моделей
- 🐳 Docker Compose (LiteLLM + PostgreSQL + Redis), ежедневные бэкапы, протестированное восстановление

---

📧 [tumasv1@gmail.com](mailto:tumasv1@gmail.com)
