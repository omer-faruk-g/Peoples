# Peoples

Peoples is a market-intelligence and persona-simulation skill for [Claude Code](https://code.claude.com). It is prompt-only: one `SKILL.md`, with no scripts and no hooks. When a product, module or user-facing feature is proposed, it makes the model look at competing products, find what their users complain about, fix those flaws in the current code, and then run a synthetic persona panel that estimates adoption and lists the main objections.

## Rules

| Section | Rule | What the model does |
|---|---|---|
| 1 | Identify competitors | It names 3–5 existing market alternatives or similar open-source or commercial products. |
| 1 | Mine negative feedback | It collects common complaints, bad reviews and UX friction points of those competitors (poor error handling, slow response, complex onboarding, missing edge cases). |
| 1 | Preemptive patching | It fixes those mined flaws in the current code or architecture before delivering the product. |
| 2 | Persona panel | It evaluates the proposal with 100–1000 synthetic personas from five groups: Tech Savvy, Beginner, Enterprise, Budget-Conscious and Security-Obsessed. |
| 2 | Scoring | Each persona gives a usability and friction score (1–10), a value proposition match (1–10) and its deal-breakers. |
| 2 | Report | It emits the `PEOPLES SIMULATION REPORT`: flaws patched in code, adopt and reject percentages, top rejection reasons, and the code change needed for 90 %+ adoption. |
| 3 | Background execution | Research and persona testing run in an isolated block or parallel thread so code generation is not delayed. Only aggregated metrics are shown, not per-agent logs. |
| 4 | Pre-flight checklist | Before delivery it checks that competitor flaws were patched, the cohort was run, and percentages and objections were calculated. |

## Install

```bash
git clone https://github.com/omer-faruk-g/Peoples ~/.claude/skills/peoples
```

Then restart Claude Code. The skill loads when a product or user-facing feature is proposed, or when you type `/peoples`.

## Limits

- The persona panel is simulated by the model. The adoption and rejection percentages are the model's estimates, not survey data from real users, and they are not a sales forecast.
- Competitor complaints are only as good as the sources the model can reach. Without web access it falls back to what it already knows.
- Nothing enforces these rules mechanically. They apply only when the skill is loaded and the model follows them.
- Competitor research and the report add tokens and time to every user-facing feature.

## Türkçe özet

Peoples, Claude Code için tek dosyalık bir skill:

- Bir ürün ya da kullanıcıya dönük bir özellik önerildiğinde 3–5 rakibi bulur.
- Rakiplerin kötü yorumlarını ve kullanıcı şikâyetlerini çıkarır, bu hataları ürünü teslim etmeden önce koda yamar.
- 100–1000 sanal persona ile (Teknik Uzman, Yeni Başlayan, Kurumsal, Bütçe Odaklı, Güvenlik Takıntılı) ürünü değerlendirir.
- Benimseme ve ret yüzdelerini, en sık ret nedenlerini ve %90+ benimseme için gereken kod değişikliğini rapor eder.

Yüzdeler modelin tahminidir, gerçek kullanıcı anketi değildir.

Kurmak için yukarıdaki `git clone` komutunu çalıştırın ve Claude Code'u yeniden başlatın.

## License

GPL-3.0-or-later. See [LICENSE](LICENSE).
