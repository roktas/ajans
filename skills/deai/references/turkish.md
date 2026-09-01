# Turkish de-AI calibration

Use this reference for Turkish de-AI work. It is not a translated English watch list, authorship detector, or drafting
checklist. Turkish morphology, information structure, evidentiality, genre, and the governing voice determine what
counts as a real problem.

If a passage is already natural, correct, source-faithful, and genre-appropriate, leave it unchanged.

## Register calibration

- **Legal and administrative prose** — Preserve required formulas, defined terms, deliberate passives, and procedural
  repetition. Remove only clusters that obscure obligations, actors, scope, or sequence.
- **Academic and institutional prose** — Preserve evidential distance, justified nominalization, conventional passives,
  and calibrated uncertainty. Reduce uniform cadence or bureaucratic padding only when it weakens the argument or hides
  responsibility.
- **Analytical and journalistic prose** — Prefer explicit logical relations and sourced concrete detail over generic
  transitions, promotional evaluation, or decorative metaphor.
- **Personal, editorial, and literary prose** — Preserve supported asides, rhetorical questions, fragments, inversion,
  dialogue, sensory detail, and tense movement when they belong to the governing voice.

Register determines which existing choices to preserve. It does not supply human markers to insert. Never invent
colloquial language, self-correction, first-person participation, dialogue, sensory detail, or a tense change merely to
create texture.

## Pattern clusters

### Inflated or generic evaluation

Review unsupported or mechanically repeated claims such as `çığır açan`, `benzersiz`, `devrim niteliğinde`, `hayati
öneme sahip`, `önemli bir dönüm noktası`, or `geleceğe ışık tutan`; stock analytical tails such as `gözler önüne
sermektedir`, `altını çizmektedir`, `ortaya koymaktadır`, `yansıtmaktadır`, or `katkı sağlamaktadır`; and generic
conclusions that restate `önem`, `potansiyel`, `sürdürülebilirlik`, or `gelecek` without adding a consequence, decision,
or fact.

Remove empty inflation, but preserve the underlying assertion at the same strength. Do not decide that a claim is
unsupported merely because its evidence is outside an isolated excerpt.

### Vague, indirect, or nominalized prose

Review:

- unnamed authorities such as `uzmanlar`, `çeşitli araştırmalar`, `sektör temsilcileri`, or `bazı çevreler` when the task
  supplies no corresponding source;
- filler transitions such as `bu bağlamda`, `bu noktada`, `öte yandan`, `bununla birlikte`, or `şunu belirtmek gerekir
  ki` when they do not express a real relation;
- chains of `-me/-ma`, `-mesi/-ması`, `gerçekleştirilmesi`, `sağlanması`, `yapılması`, and `bulunmaktadır` that hide an
  available actor or action;
- uniform `-mektedir` cadence across successive sentences when tense or register does not require it;
- excessive hedging that obscures judgment rather than preserving genuine uncertainty;
- repeated abstractions that ignore concrete actors, examples, dates, measures, or consequences already in the source.

Name an authority only when the source supplies it. Otherwise preserve the original attribution and uncertainty rather
than converting the claim into the narrator's assertion. Prefer direct verbs when actor and action are known, but do not
force an actor into scholarly, legal, or procedural passive prose.

### Formulaic rhetoric

Review repeated `yalnızca X değil, aynı zamanda Y`, `hem X hem Y`, or `bir yandan X, öte yandan Y` frames used mainly for
rhythm; authority poses such as `asıl soru`, `meselenin özü`, or `gerçekte önemli olan`; generic invitations such as
`gelin birlikte bakalım`; forced groups of three; synonym cycling; mechanically balanced clauses; slogan-like closers;
and repeated `adeta` or `sanki` comparisons that substitute atmosphere for a supported description.

State the point directly. A negative pivot often contains two claims: preserve both when both matter. Do not manufacture
roughness, fragments, archaism, or humor as proof of humanity.

### Mechanical cadence, register, and punctuation

Review runs of sentences with nearly the same length, syntax, opening, and predicate ending; repeated medium-length
sentences that package claim, qualification, and consequence in the same order; abrupt movement between bureaucratic,
technical, promotional, intimate, or literary registers; and repeated em dashes, semicolons, or inline colons that
import an English-shaped explanation pattern or conflict with the governing Turkish publication style.

Repair the underlying sentence relations. Split an overloaded sentence, combine mechanically repeated ones, or change
the order only when meaning and emphasis support the edit. Do not insert a one-line fragment merely to create sentence-
length variance.

For ordinary Turkish de-AI output, avoid em dashes unless a governing style or supplied voice requires them. Prefer
parentheses, commas, colons, or separate sentences. This is a surface preference and not evidence of authorship.

### Mechanical structure and chat residue

Review repeated bold-label lists when ordinary prose would serve better, heading-plus-paraphrase scaffolding,
unnecessary title capitalization or emoji, documentation that narrates a recent edit instead of the current system, and
assistant residue such as `Elbette`, `Harika bir soru`, `Kesinlikle haklısınız`, `Umarım yardımcı olur`, or offers to
continue embedded in the artifact.

Keep lists, headings, salutations, and correspondence conventions when the genre needs them. Remove only the wrapper
that does not belong to the artifact.

## Calibrating edits

### Deflate without deleting the claim

Before:

> Yeni sistem başvuru süresini beş günden iki güne indirerek kurumun dijital dönüşüm yolculuğunda önemli bir dönüm
> noktası oluşturmakta ve verimliliğe verilen önemi gözler önüne sermektedir.

After:

> Yeni sistem başvuru süresini beş günden iki güne indiriyor. Bu değişiklik kurumun dijital dönüşümünde önemli bir dönüm
> noktasıdır ve verimliliğe verdiği önemi gösterir.

The rewrite removes stock analytical tails while preserving the duration change, milestone claim, and asserted
importance.

### Replace a nominalization chain with its action

Before:

> Kurul tarafından başvuruların değerlendirilmesinin gerçekleştirilmesi ve sonuçların ilan edilmesinin sağlanması
> planlanmaktadır.

After:

> Kurulun başvuruları değerlendirmesi ve sonuçları ilan etmesi planlanmaktadır.

Keep the more formal form when a legal or administrative style requires it; the problem is the cluster, not any one
suffix.

### Preserve both sides of a negative pivot

Before:

> Bu yalnızca belgeleri saklayan bir arşiv değildir; kurumun ortak hafızasıdır.

After:

> Bu, hem belgeleri saklayan bir arşiv hem de kurumun ortak hafızasıdır.

Do not shorten the sentence to `Bu, kurumun ortak hafızasıdır`; that would delete the base classification.

### Repair uniform cadence without a stunt sentence

Before:

> Sistem başvuruları merkezi olarak toplamaktadır. Belgeleri otomatik olarak sınıflandırmaktadır. Eksik alanları
> kullanıcılara bildirmektedir.

After:

> Sistem başvuruları merkezi olarak toplamakta, belgeleri otomatik olarak sınıflandırmakta ve eksik alanları
> kullanıcılara bildirmektedir.

The three actions support one coordinated sentence. If the intended emphasis requires separate sentences, keep them
separate and vary only structure that has no function.

### Preserve justified passive and evidentiality

Before:

> Örneklerin analizden önce -80 °C'de saklandığı bildirilmektedir.

After:

> Örneklerin analizden önce -80 °C'de saklandığı bildirilmektedir.

The passive and evidential form preserve source status. Recasting it as a direct assertion would change attribution and
certainty.

## False positives

Do not flag prose solely because it contains passive voice, `-mektedir`, a three-item list, a rhetorical question, a
long sentence, parentheses, learned vocabulary, a repeated technical term, or one watched transition. These can be
correct Turkish and may be central to the governing voice.

Do not treat the absence of inverted sentences, rhetorical questions, short fragments, dialogue, sensory detail, first-
person forms, or tense shifts as a defect. Many natural formal texts omit all of them.

Look for repetition plus functional weakness. If an edit would make a deliberate choice more generic, keep the original.
Correct Turkish, supplied meaning, governing genre, and authorial voice outrank the desire to make a passage look less
machine-written.
