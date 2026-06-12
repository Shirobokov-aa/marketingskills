# Marketing Skills — установка и использование

44 скилла (инструкций) для AI-агентов по маркетингу: CRO, копирайтинг, SEO, реклама, аналитика, продажи и рост. Ставятся через [skills CLI](https://github.com/vercel-labs/skills).

**Важно:** скиллы работают с AI-агентом, не с редактором. VS Code сам по себе скиллы не читает — нужен Copilot, Cline, Continue и т.д.

**Фундамент:** сначала запусти `product-marketing` — он создаёт `.agents/product-marketing.md` с контекстом продукта. Остальные скиллы читают этот файл, чтобы не спрашивать одно и то же каждый раз.

---

## Скиллы по категориям

### product-marketing (начни с этого)
Контекст продукта: аудитория, позиционирование, боли клиентов, ICP. Файл: `.agents/product-marketing.md`.

**Промпты:**
```
product-marketing: опиши мой продукт по коду и README, создай контекст
```
```
product-marketing: обнови ICP и позиционирование — мы сместились на enterprise
```

### Конверсия (CRO)
| Скилл | Что делает |
|-------|------------|
| `cro` | Оптимизация лендингов и форм |
| `signup` | Регистрация и trial-активация |
| `onboarding` | Активация после регистрации |
| `popups` | Попапы, модалки, баннеры |
| `paywalls` | Экраны апгрейда в приложении |

**Промпты:**
```
cro: лендинг не конвертит — разбери и предложи улучшения
```
```
signup: оптимизируй форму регистрации, снизь отвал на шаге 2
```
```
onboarding: пользователи регистрируются, но не активируются — что менять?
```

### Контент и копирайтинг
| Скилл | Что делает |
|-------|------------|
| `copywriting` | Тексты для сайта, лендингов, pricing |
| `copy-editing` | Редактура готовых текстов |
| `cold-email` | Холодные B2B-письма и цепочки |
| `emails` | Email-воронки, welcome, drip |
| `social` | Контент для LinkedIn, X, Instagram |
| `image` | Маркетинговые изображения через AI |
| `video` | Видео через AI-инструменты |
| `sms` | SMS/MMS-маркетинг |

**Промпты:**
```
copywriting: напиши тексты для главной SaaS-продукта
```
```
emails: создай welcome-цепочку из 5 писем
```
```
cold-email: напиши холодное письмо для CTO SaaS-компаний
```

### SEO и поиск
| Скилл | Что делает |
|-------|------------|
| `seo-audit` | Технический и on-page SEO-аудит |
| `ai-seo` | Оптимизация под AI-поисковики (ChatGPT, Perplexity) |
| `programmatic-seo` | Массовая генерация SEO-страниц |
| `site-architecture` | Структура сайта, навигация, URL |
| `competitors` | Страницы сравнения с конкурентами |
| `competitor-profiling` | Исследование конкурентов по URL |
| `schema` | Schema markup и structured data |
| `aso` | App Store / Google Play |
| `directory-submissions` | Подача в каталоги (Product Hunt, G2…) |
| `content-strategy` | Контент-стратегия и темы |

**Промпты:**
```
seo-audit: проведи SEO-аудит этого сайта
```
```
ai-seo: как попасть в ответы ChatGPT и Perplexity по нашей нише?
```
```
competitors: создай страницу «Альтернатива [конкурент]»
```

### Реклама и дистрибуция
| Скилл | Что делает |
|-------|------------|
| `ads` | Google Ads, Meta, LinkedIn, TikTok |
| `ad-creative` | Массовая генерация рекламных креативов |

**Промпты:**
```
ads: помоги настроить Meta-кампанию на trial signup
```
```
ad-creative: сгенерируй 10 вариантов заголовков для Google Ads
```

### Аналитика и тесты
| Скилл | Что делает |
|-------|------------|
| `analytics` | GA4, Mixpanel, события, трекинг |
| `ab-testing` | Планирование A/B-тестов |

**Промпты:**
```
analytics: настрой GA4-события для signup и activation
```
```
ab-testing: спланируй A/B-тест на CTA главной страницы
```

### Удержание и рост
| Скилл | Что делает |
|-------|------------|
| `churn-prevention` | Отмена подписки, save offers, dunning |
| `referrals` | Реферальные и партнёрские программы |
| `free-tools` | Бесплатные инструменты для лидогенерации |
| `lead-magnets` | Лид-магниты |
| `community-marketing` | Комьюнити-маркетинг |
| `co-marketing` | Совместные кампании с партнёрами |

**Промпты:**
```
churn-prevention: спроектируй cancellation flow с save offer
```
```
referrals: как запустить реферальную программу для SaaS?
```

### Стратегия и монетизация
| Скилл | Что делает |
|-------|------------|
| `marketing-plan` | Полный маркетинговый план |
| `marketing-ideas` | 140 идей для SaaS |
| `marketing-psychology` | Психология и ментальные модели |
| `launch` | Запуск продукта / фичи |
| `pricing` | Ценообразование и монетизация |
| `customer-research` | Исследование клиентов |

**Промпты:**
```
marketing-plan: составь маркетинговый план на Q2
```
```
pricing: помоги с тарифами — freemium vs trial vs demo
```
```
launch: спланируй запуск новой фичи на Product Hunt
```

### Продажи и RevOps
| Скилл | Что делает |
|-------|------------|
| `revops` | Revenue operations, скоринг лидов |
| `sales-enablement` | Питч-деки, one-pagers, скрипты демо |
| `prospecting` | Поиск и квалификация лидов |
| `public-relations` | PR, работа со СМИ |

**Промпты:**
```
sales-enablement: создай one-pager для sales-команды
```
```
prospecting: собери список ICP-компаний для outreach
```

---

## Установка

### Только в проект (рекомендуется)

```bash
cd /path/to/your-project

# все 44 скилла
npx skills add coreyhaines31/marketingskills -a cursor -y

# выборочно
npx skills add coreyhaines31/marketingskills \
  --skill product-marketing --skill cro --skill copywriting \
  -a cursor -y

# список доступных скиллов
npx skills add coreyhaines31/marketingskills --list
```

| Область | Флаг | Куда |
|---------|------|------|
| Проект | без `-g` | `.agents/skills/` |
| Глобально | `-g` | `~/.agents/skills/` |

### Из локального клона (без GitHub)

```bash
cd /path/to/your-project
cp -r /path/to/marketingskills/skills/* .agents/skills/
```

### Cursor + VS Code сразу

Одна папка `.agents/skills/` для Cursor и Copilot/Cline:

```bash
cd /path/to/your-project

npx skills add coreyhaines31/marketingskills \
  -a cursor -a github-copilot -y
```

| Агент в VS Code | Флаг `--agent` | Папка |
|-----------------|----------------|-------|
| GitHub Copilot | `github-copilot` | `.agents/skills/` |
| Cline | `cline` | `.agents/skills/` |
| Continue | `continue` | `.continue/skills/` |
| Roo Code | `roo` | `.roo/skills/` |

Continue и Roo — отдельные папки, добавь `-a continue` или `-a roo` к команде.

### Альтернатива: SkillKit (несколько агентов)

```bash
npx skillkit install coreyhaines31/marketingskills
npx skillkit install coreyhaines31/marketingskills --skill cro copywriting
```

### Флаги

| Флаг | Значение |
|------|----------|
| `-y` / `--yes` | Без вопросов в терминале |
| `-g` / `--global` | На все проекты |
| `-a` / `--agent` | Целевой агент (`cursor`, `github-copilot`, …) |
| `--skill` | Конкретный скилл (без флага — все) |
| `--list` | Показать список скиллов без установки |

### Удалить глобальную установку

```bash
# через CLI (перечисли нужные)
npx skills remove --global product-marketing cro copywriting -a cursor -y

# или вручную — все маркетинговые скиллы разом
rm -rf ~/.agents/skills/{ab-testing,ad-creative,ads,ai-seo,analytics,aso,churn-prevention,co-marketing,cold-email,community-marketing,competitor-profiling,competitors,content-strategy,copy-editing,copywriting,cro,customer-research,directory-submissions,emails,free-tools,image,launch,lead-magnets,marketing-ideas,marketing-plan,marketing-psychology,onboarding,paywalls,popups,pricing,product-marketing,programmatic-seo,prospecting,public-relations,referrals,revops,sales-enablement,schema,seo-audit,signup,site-architecture,sms,social,video}
```

### Обновить

```bash
npx skills update
npx skills list
```

---

## Использование

1. Открой проект, где установлены скиллы.
2. **Сначала** запусти `product-marketing` — создаст контекст в `.agents/product-marketing.md`.
3. В чате агента напиши задачу и **назови скилл** в начале или в тексте.
4. Агент подхватывает скилл по `description` в `SKILL.md` — отдельная кнопка не нужна.

**Типичный порядок:**
```
product-marketing  →  контекст продукта
copywriting / cro  →  тексты и конверсия лендинга
seo-audit / schema →  SEO и разметка
analytics          →  трекинг событий
emails             →  email-воронки
```

**С AbsolutelySkilled и ui-ux-pro-max:**
```
absolute-work        →  разработка фичи
product-marketing    →  маркетинговый контекст
copywriting + cro    →  тексты и конверсия
ui-ux-pro-max        →  визуал и design system
absolute-documentations → документация
```

При похожих задачах (например, «сделай лендинг») явно указывай скилл: `@copywriting` для текстов, `@ui-ux-pro-max` для дизайна, `@cro` для конверсии.

`.agents/skills/` и `.agents/product-marketing.md` можно закоммитить в git — команда получит те же скиллы и контекст.
