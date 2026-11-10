---
marp: true
theme: default
size: 16:9
paginate: true
lang: ru
title: ИИ-ассистенты в разработке ПО
description: Как ИИ-ассистенты влияют на архитектуру команд
style: |
  section {
    background: #f7f7f1;
    color: #182f36;
    font-family: "Segoe UI", Arial, sans-serif;
    font-size: 30px;
    line-height: 1.38;
    justify-content: flex-start;
    padding: 72px 90px 76px;
  }
  section h1, section h2, section h3 {
    color: inherit;
    font-weight: 700;
    line-height: 1.12;
    letter-spacing: -0.025em;
  }
  section h1 {
    font-size: 76px;
    margin: 44px 0 22px;
  }
  section h2 {
    font-size: 53px;
    margin: 0 0 24px;
  }
  section h3 {
    font-size: 36px;
    margin: 28px 0 10px;
  }
  section p {
    margin: 0 0 20px;
  }
  section strong {
    color: #11645d;
  }
  section::after {
    font-size: 18px;
    color: #4c6167;
    right: 90px;
    bottom: 30px;
  }
  section.cover, section.summary {
    background: #112e35;
    color: #f7f7f1;
  }
  section.cover {
    justify-content: center;
  }
  section.cover h1 {
    max-width: 850px;
  }
  section.cover > p:first-child {
    color: #9ee6ce;
    font-size: 20px;
    font-weight: 700;
    letter-spacing: 0.13em;
    margin: 0;
  }
  section.cover > p:last-child {
    color: #d6e6e4;
    font-size: 40px;
    margin: 0;
  }
  section.summary strong {
    color: #9ee6ce;
  }
  section.summary::after {
    color: #c3d9d8;
  }
  section table {
    width: 100%;
    display: table;
    table-layout: fixed;
    margin: 12px 0 25px;
  }
  section table tr,
  section table tr:nth-child(2n) {
    background: transparent;
    border: 0;
  }
  section table th,
  section table td {
    border: 0;
    padding: 15px 24px 15px 0;
    vertical-align: top;
  }
  section table td {
    border-top: 1px solid #b9cac6;
  }
  section.stats table {
    margin-top: 22px;
  }
  section.stats th {
    color: #11645d;
    font-size: 85px;
    line-height: 1.05;
    letter-spacing: -0.05em;
    font-variant-numeric: tabular-nums;
  }
  section.stats td {
    font-size: 29px;
  }
  section.stats > p:last-of-type {
    color: #4c6167;
    font-size: 24px;
    font-style: normal;
  }
  section.screenshot img {
    display: block;
    max-width: 100%;
    max-height: 420px;
    width: auto;
    height: auto;
  }
  section.screenshot > p:last-of-type {
    color: #4c6167;
    font-size: 26px;
    margin-bottom: 0;
  }
  section.agent-shot p:has(img) {
    position: relative;
    width: 800px;
    height: 435px;
    overflow: hidden;
  }
  section.agent-shot img {
    position: absolute;
    top: -37px;
    left: -312px;
    width: 1114px;
    max-width: none;
    max-height: none;
  }
  section ul, section ol {
    padding-left: 1.2em;
    margin: 10px 0 24px;
  }
  section li {
    padding-left: 0.18em;
    margin-bottom: 16px;
  }
  section li::marker {
    color: #11645d;
  }
  section.summary li::marker {
    color: #9ee6ce;
  }
  section.example blockquote, section.summary blockquote {
    border-left: 4px solid #11645d;
    padding: 4px 0 4px 24px;
    margin: 0 0 26px;
    color: inherit;
    font-size: 32px;
  }
  section.summary blockquote {
    border-color: #9ee6ce;
    margin: 32px 0 0;
  }
  section.example blockquote p, section.summary blockquote p {
    margin: 0;
  }
---

<!-- _class: cover -->
<!-- _paginate: false -->

АРХИТЕКТУРА ПО

# ИИ-ассистенты в разработке ПО

Влияние на архитектуру команд

---

<!-- _class: screenshot -->

## Автодополнение в редакторе

![VS Code. Copilot предлагает тело функции calculateDaysBetweenDates серым текстом](assets/inline-suggestion.png)

Серым показан код, который Copilot предлагает дописать.

---

<!-- _class: screenshot -->

## Чат с ассистентом

![VS Code. В ответ на вопрос о пяти самых больших файлах Copilot предлагает команду PowerShell](assets/copilot-chat.png)

Copilot предлагает команду для поиска пяти самых больших файлов в проекте. Разработчик решает, запускать ли её.

---

<!-- _class: screenshot agent-shot -->

## Агент в VS Code

![VS Code. Агент изменил HTML, JavaScript и CSS и просит разрешение запустить проверку](assets/copilot-agent.png)

Агент создал три файла и запросил разрешение на запуск проверки.

---

<!-- _class: example -->

## Задача для агента

> При создании записи пустое название должно давать ответ HTTP 400. Добавь тест. Сохрани формат ответа при успешном запросе.

- **Агент** находит проверку в репозитории, правит её и запускает тесты.
- **Разработчик** проверяет ответ и при пустом названии, и при обычном запросе.

---

## Примеры GitHub и Spotify

### GitHub

Copilot убирает устаревшие флаги функций и открывает PR. Инженеры проверяют изменения и решают, можно ли их принять.

### Spotify

Honk готовил PR для перехода на новые версии наборов данных. Там, где не хватало автоматических тестов, команды вручную проверяли правки в своих репозиториях.

---

<!-- _class: stats -->

## Что изменилось после внедрения агентов

Через год после внедрения. Исследование охватило 655 компаний.

| +35,7% | +56,1% | +13,7% |
| :--- | :--- | :--- |
| Новых запросов на слияние (PR) | К среднему времени от открытия PR до слияния | Закрытых задач в Jira |

Число PR и задач измеряли на сотрудника в месяц. Рост числа закрытых задач статистически незначим при пороге 5%.

---

## Что меняется в команде

- **Команда сервиса** задаёт требования к правке агента и отвечает за её ревью и выпуск.
- **Платформенная команда** настраивает доступ агента к репозиториям и общие автоматические проверки.
- **Владельцы связанных сервисов** согласуют изменения API. Описание API и тесты в репозитории помогают агенту соблюдать договорённости.

---

<!-- _class: summary -->

## Как понять, что ассистент помог

Один сервис, сопоставимые задачи до и во время пилота.

- **Время до первого ревью** показывает, растёт ли очередь.
- **Время от коммита до выпуска** показывает, ускорилась ли поставка.
- **Доля выпусков, потребовавших вмешательства** помогает оценить стабильность.

> Польза для команды видна, когда проверенные изменения быстрее доходят до пользователей, а стабильность сохраняется.
