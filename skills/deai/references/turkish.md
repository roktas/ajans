# Turkish de-AI calibration

Use these as review signals, not banned forms. Turkish morphology, information structure, evidentiality, genre, and the
supplied voice determine whether a pattern is actually weak.

## Pattern clusters

- **Inflated evaluation** — Repeated unsupported or decorative phrases such as `çığır açan`, `benzersiz`, `hayati öneme
  sahip`, `önemli bir dönüm noktası`, `gözler önüne sermektedir`, or similar stock tails that add no new relation.
- **Vague attribution** — `uzmanlar`, `çeşitli araştırmalar`, `bazı çevreler`, or similar unnamed authorities when the
  task provides no such source. Do not invent a named authority to repair them.
- **Nominalized chains** — Repeated `-me/-ma`, `-mesi/-ması`, `gerçekleştirilmesi`, `sağlanması`, `yapılması`, or
  `bulunmaktadır` constructions that hide an available actor or action.
- **Mechanical cadence** — Uniform `-mektedir` predicates, repeated sentence shapes, or identical claim-qualification-
  consequence sequences when the material does not require that parallelism.
- **Formulaic rhetoric** — Repeated `yalnızca X değil, aynı zamanda Y`, `bir yandan X, öte yandan Y`, forced groups of
  three, slogan-like closers, vague `asıl soru` or `meselenin özü` poses, and generic invitations such as `gelin birlikte
  bakalım` when they serve presentation rather than meaning.
- **Generic transitions** — Repeated `bu bağlamda`, `bu noktada`, `öte yandan`, `bununla birlikte`, or `şunu belirtmek
  gerekir ki` where no real causal, contrastive, conditional, or sequential relation is being expressed.
- **Chat residue** — `Elbette`, generic praise, `Umarım yardımcı olur`, offers to continue, decorative emoji, or other
  assistant wrapper embedded in a document.
- **Imported punctuation** — Repeated em dashes, semicolons, inline colons, or English-shaped explanatory structures when
  they conflict with the governing Turkish publication style or have no functional role.

## False positives

Do not flag prose merely because it contains passive voice, `-mektedir`, a three-item list, a rhetorical question, a long
sentence, parentheses, learned vocabulary, a repeated technical term, or one watched transition. Many natural formal
Turkish texts use all of these. Do not manufacture inverted sentences, fragments, dialogue, slang, humor, sensory detail,
first-person forms, or tense shifts merely to create texture.
