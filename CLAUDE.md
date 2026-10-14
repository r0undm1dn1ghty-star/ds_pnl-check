# CLAUDE.md — работа с репозиторием P&L Check

## Структура

```
ds_pnl-check/
├── README.md                  ← главный документ (русский)
├── LICENSE                    ← Apache 2.0
├── NOTICE.md                  ← условия работы с источниками
├── AGENTS.md                  ← инструкция для агента
├── SAFETY_RAILS.md            ← стоп-правила
├── DATA_EVIDENCE_STANDARD.md  ← стандарт доказательств
├── skills/ds_pnl-check/          ← переносимый skill
├── templates/                 ← опросник, структура P&L, шаблоны
├── integrations/              ← адаптеры (Claude Code, MCP, ChatGPT)
├── docs/ru/                   ← документация на русском
├── docs/en/                   ← английское изложение
└── tests/                     ← проверки структуры
```

## Правила работы

1. **Русский — основной язык.** Английский — для международных разработчиков.
2. **Не смешивай с методологией Замесина (CC BY-NC-SA).** P&L Check — независимый Apache-2.0 инструмент.
3. **Не включай конфиденциальное:** клиентские данные, реквизиты, пароли, `internal/`.
4. **Перед push** — проверки: `tests/check_markdown_links.py`, `tests/validate_public_release.py`, `git grep` на секреты.
5. **Не публикуй обещания** о сегменте/цене/эффекте до design-partner проверок.

## Команды

```bash
# Проверка структуры
python3 tests/check_markdown_links.py
python3 tests/validate_public_release.py

# Проверка на секреты
git grep -n -i -E 'пароль|password|token|api[_-]?key|паспорт|реквизит' -- ':!internal'
```
