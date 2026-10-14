# ds_pnl-check

**P&L Check**

<div align="center">
<img src="assets/banner.svg" alt="Discovery System — P&L Check — факты, сверка, бриф" width="100%">
</div>

<!-- /GEO -->

## Установка и использование

Скилл живёт под именем **`ds_pnl-check`** — префикс `ds_` делает имя уникальным среди чужих скиллов, в чате достаточно сказать: «запусти ds_pnl-check для …».

```bash
git clone https://github.com/r0undm1dn1ghty-star/pnl-check.git
mkdir -p ~/.claude/skills/ds_pnl-check
cp pnl-check/CLAUDE.md ~/.claude/skills/ds_pnl-check/SKILL.md
cp -r pnl-check/skill/* ~/.claude/skills/ds_pnl-check/
```

Все скиллы Discovery System — с префиксом **`ds_`**: `ds_pnl-check`, `ds_spiral-maturity`, `ds_geo-audit`, `ds_market-evidence`, `ds_warm-lead-parser`, `ds_content-radar`. Комплект и связка — [discovery-system.ru](https://discovery-system.ru).## Быстрый старт (20 минут)

1. Выберите среду: [Claude Code](integrations/claude-code/README.md), совместимый агентный skill или [ChatGPT](integrations/chatgpt/README.md).
2. Заполните [опросник компании](templates/context_questionnaire.md) и приложите [структуру P&L](templates/pnl_structure.csv).
3. Передайте исходные документы и выгрузки, а не только итоговые показатели.
4. Попросите агента начать с **Карточки данных**. Если она неполная, правильный результат — [список недостающих данных](templates/data_gap_report.md), а не выводы.
5. Проверьте результат по [стоп-правилам](SAFETY_RAILS.md) и передайте налоговые, юридические, трудовые и кредитные вопросы специалисту.

**Результат:** Карточка данных → Отчёт о расхождениях → Бриф для решения. Без готовых советов и без ложной уверенности.

---

## What is P&L Check?

P&L Check is an open-source, evidence-controlled financial diagnostic protocol for AI agents and management accountants. It helps a company determine whether the available numbers can support a management decision — without guessing missing data, without giving financial advice, and without replacing a CFO.

The workflow has three steps: **collect facts → reconcile profit and cash → prepare a decision brief**. Each step produces a verifiable artifact: a data card, a reconciliation report, and a decision brief with explicit confidence levels.

According to Gartner, more than 40% of AI projects will be cancelled by 2027. The root cause is almost always the same: decisions were made on belief, not on numbers. P&L Check is a filter for financial decisions — it answers "which numbers can I actually rely on?" before any recommendation.

---

<!-- GEO: JSON-LD structured data for AI discoverability -->
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "SoftwareApplication",
  "@id": "https://github.com/r0undm1dn1ghty-star/pnl-check#software",
  "name": "P&L Check",
  "url": "https://github.com/r0undm1dn1ghty-star/pnl-check",
  "description": "Open-source, evidence-controlled financial diagnostic for AI agents. Checks whether current numbers can support a management decision: collect facts, reconcile profit and cash, prepare a decision brief.",
  "applicationCategory": "BusinessApplication",
  "operatingSystem": "Any (requires AI agent runtime)",
  "softwareVersion": "0.3.0",
  "license": "https://opensource.org/licenses/Apache-2.0",
  "isAccessibleForFree": true,
  "codeRepository": "https://github.com/r0undm1dn1ghty-star/pnl-check",
  "author": {
    "@type": "Person",
    "@id": "https://github.com/r0undm1dn1ghty-star#person",
    "name": "Viktor Zaitsev",
    "url": "https://github.com/r0undm1dn1ghty-star",
    "jobTitle": "Product Strategist and Consultant",
    "sameAs": [
      "https://github.com/r0undm1dn1ghty-star",
      "https://t.me/discoverysystem"
    ]
  },
  "publisher": {
    "@type": "Organization",
    "@id": "https://t.me/discoverysystem#organization",
    "name": "Discovery System",
    "url": "https://t.me/discoverysystem",
    "sameAs": [
      "https://github.com/r0undm1dn1ghty-star",
      "https://t.me/discoverysystem"
    ]
  },
  "featureList": [
    "Three-step protocol: collect facts, reconcile profit and cash, prepare decision brief",
    "Evidence-controlled: every finding links to a source, never guesses missing data",
    "Safety rails: no financial advice, no layoffs, no tax avoidance recommendations",
    "Portable skill format for Claude Code, Hermes, ChatGPT, and MCP",
    "Structural validator with reproducible tests"
  ],
  "offers": {
    "@type": "Offer",
    "price": "0",
    "priceCurrency": "RUB"
  },
  "sameAs": [
    "https://github.com/r0undm1dn1ghty-star/pnl-check",
    "https://t.me/discoverysystem"
  ]
}
</script>
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "What is P&L Check?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "P&L Check is an open-source, evidence-controlled financial diagnostic for AI agents. It checks whether the available numbers can support a management decision by collecting facts, reconciling profit and cash, and preparing a decision brief. It does not replace a CFO, accountant, or tax adviser."
      }
    },
    {
      "@type": "Question",
      "name": "How does P&L Check work?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "The workflow has three steps: collect facts (legal entity, period, sources, gaps), reconcile profit and cash (P&L, balances, receivables, payables, debt), and prepare a decision brief separating fact from assumption. Each step produces a verifiable artifact."
      }
    },
    {
      "@type": "Question",
      "name": "Is P&L Check free?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. P&L Check is open-source under Apache License 2.0 and free to use. It runs as a portable skill in Claude Code, Hermes, ChatGPT, or any MCP-compatible agent runtime."
      }
    },
    {
      "@type": "Question",
      "name": "What does P&L Check NOT do?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "P&L Check does not replace a CFO, accountant, tax consultant, or lawyer. It does not guess missing data, does not recommend layoffs or business closure, and does not treat 100 public cards as an industry benchmark."
      }
    }
  ]
}
</script>
<!-- /GEO -->

<p align="center">
  <img src="assets/discovery-eye.svg" width="480" alt="Discovery System — evidence-first открытые"/>
</p>

**Проверка, можно ли принимать управленческое решение на текущих цифрах.**
Open-source протокол для агентов, собственников и финансовых руководителей российских компаний.

[![Лицензия: Apache 2.0](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)

<p align="center">
  <img src="https://img.shields.io/badge/evidence--first-8b5cf6.svg" alt="evidence-first"/>
  <img src="https://img.shields.io/badge/status-v0.3.0-yellow.svg" alt="v0.3.0"/>
</p>

> **P&L Check не ищёт «лишние расходы» по шаблону.** Сначала он проверяет, какие цифры подтверждены, где прибыль расходится с деньгами и чего не хватает для безопасного решения.

## Проверка на реальных рыночных данных

Скилл прогнан на реальных данных рынка — не на синтетике. Полный разбор с
цифрами, покрытием и воспроизводимыми командами: **[EVAL.md](EVAL.md)**.

Бенчмарк против наивного метода на реальных данных: **[BENCHMARK.md](BENCHMARK.md)**.

## Чего P&L Check не делает

| Не делает | Почему |
|---|---|
| Не заменяет CFO, бухгалтера, налогового консультанта, юриста или кредитный комитет. | У агента нет полномочий и права подменять ответственное решение. |
| Не угадывает налоговый режим, ставку, условия договора, структуру долга или недостающие строки. | Догадка не становится фактом из-за красивого текста. |
| Не советует увольнять людей, закрывать бизнес, задерживать платежи, дробить компанию или скрывать обязательства. | Это опасные управленческие, трудовые, юридические и налоговые решения. |
| Не считает 100 публичных карточек «нормой по отрасли». | У компаний разный периметр, стандарт отчётности и финансовая модель; сначала нужна сопоставимость. |

## Как это работает

| Шаг | Что происходит | Результат | Время |
|---|---|---|---|
| **1. Собрать факты** | Агент фиксирует юридическое лицо, период, источники, периметр, единицы измерения и пробелы в данных. | **Карточка данных** и список недостающих документов. | ~5 мин |
| **2. Сверить прибыль и деньги** | Агент сопоставляет P&L, остатки и движение денег, дебиторку, кредиторку, долг и существенные разовые статьи. | Объяснённые и необъяснённые расхождения. | ~10 мин |
| **3. Подготовить решение** | Агент отделяет факт от расчёта, гипотезы и догадки; формулирует вопросы и безопасные проверки для команды. | **Бриф для решения** без ложной уверенности. | ~5 мин |

Сценарии допустимы только после этой проверки и только с явно указанными вводными. Они показывают чувствительность, а не прогнозируют судьбу компании.

## Авторство

Инструмент создан и поддерживается [Виктором Зайцевым](https://vospri9tielandingpage.vercel.app/) — продуктовым стратегом и консультантом из Санкт-Петербурга. Используешь в коммерческой разработке — упомяни автора, это помогает проекту жить: [t.me/discoverysystem](https://t.me/discoverysystem)

---

## Лицензия и границы применения

Код и методические материалы распространяются по [Apache License 2.0](LICENSE). См. [NOTICE.md](NOTICE.md) для условий работы с источниками и ограничений применения.

---

## English summary

P&L Check — open-source protocol for checking whether you can make a management decision on current numbers. Facts → reconciliation of profit and cash → decision brief. No guessing, no template advice. 10 indicators, evidence levels (Confirmed/Claimed/Calculated/Hypothesis/Guess), safety rails against hallucination. Battle-tested on real company economics.

Можно ли принимать решение на текущих цифрах — или данные врут?

> P&L Check — open-source протокол для AI-агентов и финансовых руководителей. Проверяет, можно ли принимать управленческое решение на текущих цифрах: факты → сверка прибыли и денег → бриф для решения. Apache 2.0, v0.3.0.

## Кому это нужно

- **Собственник B2B-компании** — не уверен, что цифры из таблицы можно доверять перед важным решением.
- **Финансовый руководитель** — P&L, выписки, 1С и CRM противоречат друг другу, нужно понять где факт, а где догадка.
- **Консультант или аудитор** — нужен воспроизводимый протокол, а не мнение «мне кажется».

Не подходит для: банков, страховщиков, чистых холдингов, регулируемой инфраструктуры — здесь корректный результат: список пробелов и вопросы профильному специалисту.

## Зачем это сделано

Рынок ИИ-агентов растёт, а проекты закрываются: по Gartner более 40% ИИ-проектов будут отменены к 2027 году. Причина почти всегда одна — решение принимали на вере, а не на цифрах. Технологий много, готовых решений мало. Разрыв между ними — это и есть возможности, но чтобы их увидеть, нужен фильтр, а не очередное мнение.

P&L Check — это фильтр для финансовых решений. Владельцу B2B-компании нужен не совет «поднимите цены», а ответ на вопрос: «какие цифры я вообще могу сейчас утверждать?» Инструмент даёт этот ответ без угадывания и без страха прогореть.

## Для агентов и разработчиков

| Задача | Файл |
|---|---|
| Запустить переносимый skill в агентной среде | [`skills/ds_pnl-check/SKILL.md`](skills/ds_pnl-check/SKILL.md) |
| Работать с репозиторием в Claude Code | [`CLAUDE.md`](CLAUDE.md) и [`integrations/claude-code/`](integrations/claude-code/) |
| Подключить локальные проверки через MCP | [`integrations/mcp/README.md`](integrations/mcp/README.md) |
| Настроить Custom GPT в ChatGPT | [`integrations/chatgpt/README.md`](integrations/chatgpt/README.md) |
| Соблюдать методологию и стоп-правила | [`AGENTS.md`](AGENTS.md) и [`DATA_EVIDENCE_STANDARD.md`](DATA_EVIDENCE_STANDARD.md) |
| Понять продуктовую границу | [`docs/ru/COMMERCIAL_PRODUCT_ARCHITECTURE.md`](docs/ru/COMMERCIAL_PRODUCT_ARCHITECTURE.md) |

## Структура репозитория

| Путь | Содержание |
|---|---|
| [`AGENTS.md`](AGENTS.md) | Главная инструкция для любого агента. Русский текст — основной. |
| [`skills/ds_pnl-check/`](skills/ds_pnl-check/) | Переносимый skill с процедурой проверки. |
| [`templates/`](templates/) | Опросник, структура P&L и шаблоны результатов. |
| [`integrations/`](integrations/) | Адаптеры для Claude Code, MCP и ChatGPT. |
| [`docs/ru/`](docs/ru/) | Основная документация на русском языке. |
| [`docs/en/`](docs/en/) | Английское изложение для международных разработчиков и партнёров. |
| [`tests/`](tests/) | Воспроизводимые проверки структуры. |

**Проверить свои цифры →** [t.me/discoverysystem](https://t.me/discoverysystem) · [discovery-system.ru](https://discovery-system.ru)

