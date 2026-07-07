## Михаил Тумасов

Архитектор LLM-слоя и AI Technical Manager. 9+ лет в IT: системный аналитик -> проджект -> руководитель отдела из 18 аналитиков в финтех. Сейчас проектирую и строю LLM-инфраструктуру целиком, от архитектурных решений до продакшн на собственном сервере.

Ищу роль на стыке архитектуры и управления: AI Technical Manager, AI Product Manager, архитектор LLM-слоя.

### LLM-контур, который я спроектировал и держу в проде

Проекты ниже складываются в единую платформу. Тот же набор слоев строят внутренние LLM-команды крупных компаний:

```
 приложения: RAG-агент, Telegram-боты, Harness агенты
      |
 LLM-шлюз (LiteLLM): маршрутизация, fallback, бюджеты
      |
 провайдеры: OpenRouter, DeepSeek и др.
      |
 observability: Langfuse (трейсы) + Prometheus/Grafana (метрики)
```

Каждое архитектурное решение записано с альтернативами и trade-offs: только в проекте Agentic-RAG 16 ADR.

**[Agentic-RAG](https://github.com/tumasv1/RAGv2-Agentic-RAG)**: агентный RAG-ассистент по базе знаний Obsidian.
Async LangGraph ReAct-агент с гибридным поиском (dense e5-large + BM25 + RRF fusion), Parent-Child чанкинг, кросс-энкодер reranking, guardrails против зацикливания и галлюцинаций. Качество измеряю, а не оцениваю на глаз: RAGAS на 18 golden set, faithfulness 0.85.

**[LLM Gateway](https://github.com/tumasv1/LLM-gateway)**: единая точка доступа ко всем LLM-провайдерам.
LiteLLM Proxy с маршрутизацией и fallback. Виртуальные ключи с бюджетами и лимитами rpm/tpm по проектам, учет расходов в PostgreSQL. Через шлюз ходят все AI-инструменты.

**[Langfuse](https://github.com/tumasv1/Langfuse)**: self-hosted трейсинг LLM-запросов.
Полный стек v3 (ClickHouse, PostgreSQL, Redis, MinIO) в изолированном LXC. Два источника трейсов в один проект: шлюз дает плоские вызовы, LangGraph-агент отдает полное дерево диалога. Видно, на каком шаге агент что происходит и сколько стоит каждый ответ.

Плюс несколько проектов поменьше: [Telegram-бот](https://github.com/tumasv1/bot-speech2text) для транскрибации встреч с диаризацией спикеров и авто-резюме, и автономный AI-агент с интеграциями Mail, Calendar и Obsidian (через собственный MCP-сервер).

### Стек

LangGraph / LangChain, RAGAS, LiteLLM, Langfuse, MCP, FastAPI, Qdrant, PostgreSQL, Redis, Docker, Grafana, Python.

### Что я умею как управленец

- Руководил группой из 18 аналитиков, за год вырастил ее на 70%
- Выстроил процессы: SDLC, SLA, оценка трудозатрат, онбординг, вторая линия поддержки


---

Telegram: [@MikhailTumasov](https://t.me/MikhailTumasov) · Почта: tumasv1@gmail.com
