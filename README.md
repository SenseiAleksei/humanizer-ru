# humanizer-ru

Скилл для Claude, который убирает признаки ИИ из текста на русском и английском.
Основан на [humanizer](https://github.com/blader/humanizer) Siqi Chen: там правила для английского,
здесь к ним добавлен файл `ru.md` с русскими правилами.

[English below](#english)

## Что делает

Находит в тексте приёмы, по которым видно, что писала нейросеть, и переписывает текст так, чтобы смысл
остался прежним. Для русского отдельно разобраны:

- канцелярит: «является», «осуществлять контроль», «в рамках», «данный», цепочки родительных падежей;
- «не просто X, а Y» и «это не про X, это про Y»;
- подводки вроде «давайте разберёмся» и «важно отметить, что»;
- слова-маркеры: ключевой, уникальный, экосистема, раскрыть потенциал, в современном мире;
- кальки с английского: «адресовать проблему», «на ежедневной основе», «в конце дня»;
- пустые выводы и чат-обёртки: «таким образом», «надеюсь, это поможет!».

Чего скилл не трогает: грамматические тире («Москва — столица России»), ёлочки «», дефисы по орфографии
и манеру автора. Если человек пишет на «ты», со сленгом или матом, текст таким и останется.

## Пример

**Было:**
> В современном мире искусственный интеллект играет ключевую роль в трансформации бизнеса. Важно отметить,
> что это не просто тренд — это фундаментальный сдвиг. Компании, которые осуществляют внедрение
> ИИ-решений, получают уникальные конкурентные преимущества: скорость, эффективность и масштабируемость.
> Таким образом, ИИ открывает новые горизонты для развития.

**Стало:**
> ИИ сильно меняет то, как работают компании. Те, кто его внедрил, работают быстрее и легче растут.

**Было:**
> Данное решение является эффективным инструментом, позволяющим осуществлять мониторинг показателей
> в рамках повседневной деятельности компании.

**Стало:**
> С этим инструментом компания каждый день видит свои показатели.

## Установка

Claude Code:

```bash
git clone https://github.com/SenseiAleksei/humanizer-ru ~/.claude/skills/humanizer-ru
```

В приложении Claude (claude.ai) скилл можно загрузить архивом в настройках, в разделе Skills.

## Как пользоваться

Попросите Claude: «прогони через humanizer», «убери признаки ИИ», «сделай текст живым» и вставьте текст.
Если дать образец своего текста, скилл подстроится под вашу манеру.

## Лицензия

MIT. Английские правила: Siqi Chen, [blader/humanizer](https://github.com/blader/humanizer).
Русские правила: SenseiAleksei.

---

## English

A Claude skill that removes signs of AI writing from Russian and English text. It is based on
[humanizer](https://github.com/blader/humanizer) by Siqi Chen, which covers English; this repo adds
`ru.md` with rules for Russian.

The Russian rules cover bureaucratic style (канцелярит), the Russian "not X but Y", stock AI words,
English calques, staged openers, empty conclusions and chatbot wrappers. They keep what is correct in Russian:
grammatical dashes, «» quotes, hyphens required by spelling, and the author's register.

Install for Claude Code:

```bash
git clone https://github.com/SenseiAleksei/humanizer-ru ~/.claude/skills/humanizer-ru
```

License: MIT. English rules by Siqi Chen; Russian rules by SenseiAleksei.
