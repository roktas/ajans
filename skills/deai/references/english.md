# English de-AI calibration

Use this reference for English de-AI work. It is a revision guide, not an authorship detector or a banned-form list.
Follow the source's genre, publication rules, terminology, and supplied voice first.

## Register calibration

- **Scholarly and scientific prose** — Preserve epistemic modals, warranted hedging, evidential distance, defined terms,
  functional passives and nominalizations, parallel structure, citations, and useful semicolons. Remove formulaic prose
  only when it weakens the claim, evidence relation, actor, scope, or argument.
- **Technical prose and documentation** — Preserve domain terms, exact conditions, stable terminology, scannable
  structure, commands, identifiers, and supported operational detail. Remove generic tutorial framing, promotional
  adjectives, and diff narration rather than inventing engineer slang or production experience.
- **Legal, policy, and reference prose** — Preserve defined terms, required formulas, deliberate repetition, calibrated
  obligation, and conventional passives. Directness must not change legal or evidential force.
- **Professional correspondence** — Make the purpose and request easy to find. Remove rote pleasantries, generic offers,
  and assistant scaffolding only when they are not genuine relationship work.
- **Personal, editorial, and literary prose** — Preserve supported asides, rhetorical questions, fragments, recurrence,
  deliberate imbalance, humor, and distinctive punctuation when they belong to the governing voice. Do not manufacture
  them where none exists.

Register tells you what to preserve. It does not supply human markers to insert.

## Pattern clusters

### Assistant-shaped discourse

Review repeated structures that make a document sound like a helpful chat response instead of its intended genre:

- helper preambles such as `here's how I'd think about it`, `I'd frame this as`, or `there are a few things to consider`;
- unrequested option catalogs, obvious definitions, or step lists that merely enumerate what the reader already knows;
- self-narrating transitions such as `in this section`, `as we'll see`, or `let me walk you through` when structure already
  supplies the orientation;
- a claim followed mechanically by a caveat, recap, reassurance, and offer to continue;
- approval seeking, generic praise, knowledge-cutoff disclaimers, or closers such as `I hope this helps` embedded in the
  artifact.

Remove the assistant wrapper, not the substantive caution or real relationship work. Genuine signposting remains useful
in long, technical, or nonlinear documents.

### Inflated significance, promotion, and superficial analysis

Review clusters of:

- broad significance or legacy claims that could fit almost any subject: `pivotal`, `vital`, `enduring`, `stands as`,
  `serves as`, `testament`, `evolving landscape`, or generic broader-trend framing;
- promotional wording such as `vibrant`, `renowned`, `groundbreaking`, `breathtaking`, `robust`, or `powerful` when it
  substitutes evaluation for a supported property;
- participial tails such as `highlighting`, `underscoring`, `reflecting`, `showcasing`, `fostering`, or `ensuring` when
  they append vague analysis rather than a sourced relation;
- generic `Challenges`, `Future outlook`, impact, potential, or conclusion sections that restate importance instead of
  adding a consequence, decision, fact, or limitation;
- lists of media mentions, followers, awards, or authorities used as substitutes for the relevant supported point.

Remove empty inflation, but preserve the underlying assertion at the same strength. An isolated excerpt can omit the
support for a claim; lack of visible evidence is not itself authority to delete or weaken it.

### Vague attribution and speculative gap filling

Review unnamed authorities such as `experts argue`, `observers note`, `industry reports`, or `some critics`, and prose
that fills missing knowledge with plausible biography, motive, impact, or current status.

When the source supplies an authority, name it if doing so improves the text. Otherwise preserve the original attribution
and uncertainty rather than converting the sentence into the narrator's assertion. Flag an evidentiary problem
separately when the task requires source review; never invent a citation or authority as a stylistic repair.

### Announced insight and rhetorical scaffolding

Review repeated presentation formulas such as:

- `the key insight`, `the real question`, `what really matters`, `at its core`, or `the deeper issue` when the next clause
  can state the point directly;
- `what surprised me was`, `the pattern is`, or `it turns out` when the announcement adds no supported perspective;
- performative emphasis such as `make no mistake`, `let that sink in`, `full stop`, or `I promise` when it only repeats a
  claim;
- lesson-like paragraph endings, standalone wisdom, aphorism templates, or manufactured punchlines that replace a
  concrete consequence or action.

Lead with the actual event, claim, condition, or consequence. Preserve real surprise, emphasis, or authorial stance when
it is part of the source.

### Mechanical balance and negative pivots

Review repeated:

- `not only X but Y`, `not X but Y`, `X rather than Y`, and other negative pivots used mainly for rhythm;
- forced groups of three, mirrored clauses, chiasmus, identical paragraph arcs, or mechanically paired parentheticals;
- symmetric `on one hand ... on the other hand` framing when the evidence or decision is materially asymmetric;
- synonym cycling introduced only to avoid repetition.

Repair the mechanical structure without deleting a real distinction. A negative pivot often contains two claims; keep
both when both matter. Balanced analysis is legitimate when the evidence is genuinely balanced.

### Mechanical cadence

Review runs of sentences with nearly identical length, syntax, openings, clause order, or endings. Also review repeated
short fragments used as punchlines, repeated colon reveals, and repeated punctuation performing the same dramatic or
explanatory job.

Repair the sentence relationships rather than chasing numerical variation. Split, combine, or reorder only when the
content supports the change. Do not impose sentence-length targets or punctuation quotas.

### Detector-sensitive typography

Some downstream AI detectors overweight surface typography. For explicit de-AI output, normalize these features when no
stronger house style, publication rule, quoted-source requirement, or supplied voice requires them:

- Prefer commas, parentheses, colons, or separate sentences to an em dash (`—`). Avoid introducing new em dashes and
  replace existing ones when the same relation can be expressed naturally without changing cadence or meaning.
- Prefer straight ASCII quotation marks and apostrophes (`"` and `'`) to curly forms (`“ ”` and `‘ ’`) in editable prose.
  Do not alter protected quotations, exact source text, publisher-mandated typography, or code-like material merely for
  normalization.

These are output-normalization preferences, not evidence of AI authorship. Do not report an em dash or curly quote as a
finding by itself, and do not damage a governing style to remove one.

### Lexical inflation and referential drift

Review:

- generic high-register verbs, ornamental modifiers, padded transitions, and abstract nouns that recur without adding
  precision;
- elaborate substitutes for basic copulas, such as repeated `serves as`, `stands as`, `marks`, `represents`, or `boasts`,
  when `is`, `has`, or a direct verb carries the same claim;
- consultancy and management metaphors such as `navigate`, `lean into`, `circle back`, or abstract `landscape` when a
  more exact ordinary or domain-native word exists;
- near-synonym rotation for the same referent, such as alternating `company`, `firm`, and `organization` merely for
  variety.

Prefer the exact ordinary or domain-native word supported by context. No word is prohibited independently of meaning,
register, repetition, and function. Stable terminology is usually more natural than decorative lexical diversity.

### Specificity, agency, and metonymy

Use concrete actors, examples, dates, measures, tools, and consequences already supplied by the source when abstract
prose unnecessarily hides them. If the source lacks such anchors, keep the prose appropriately general.

Review false-agency constructions when an abstraction hides a supplied material actor: `the decision emerged`, `the
conversation moved`, `the complaint became a fix`. Name the actor when the source identifies one. Preserve precise,
conventional metonymy such as `the study shows`, `the court held`, or `the market fell`; replacing it with an invented or
irrelevant person is worse.

### Mechanical structure, formatting, and diff narration

Review:

- repeated bold-label lists when ordinary prose or a simpler list better serves the reader;
- headings followed by one-line paraphrases before the real content;
- unnecessary title capitalization, decorative emoji, repeated thematic breaks, or chat formatting carried into a
  document;
- prose that narrates the editing process or recent diff instead of describing the current state;
- markup or citation artifacts accidentally copied from an assistant response.

Keep lists, headings, formatting, and change history when the genre or task actually requires them. The problem is not
the visible form but its lack of communicative function.

### Performed register

Review surface markers pasted onto a conflicting structure: casual contractions over a status-report arc, engineer slang
over generic advice, intimacy over unsupported first-person claims, deliberate lowercase text over formal exposition, or
formal vocabulary alternating with promotional copy without a change in speaker or purpose.

Resolve the structural register mismatch using choices already licensed by the artifact, channel, or supplied sample. Do
not add roughness, profanity, fashionable jargon, typos, or personal participation to perform authenticity.

## Rewrite calibration

1. Extract the passage's claims, qualifications, evidence, relationships, required terms, and protected voice choices.
2. For a dense cluster, reconstruct the affected passage from those obligations rather than performing a chain of local
   synonym substitutions. Keep unaffected prose intact.
3. Preserve genuine balance, uncertainty, politeness, repetition, and formal structure. Do not choose a side or add a
   personal stance unless the source or user supplies that authority.
4. Apply detector-sensitive typography only after semantic and stylistic repairs, so punctuation normalization does not
   drive the rewrite.
5. Inspect the actual revision for repeated openings, announcement structures, helper framing, cadence runs, formulaic
   closers, and synonym cycling regenerated during rewriting.
6. Stop when the prose is natural, correct, genre-appropriate, and faithful.

## Calibrating examples

Use these examples to calibrate transformations, not as phrases or topics to copy. Every rewrite must stay within the
facts, claims, uncertainty, and voice supplied by the input. If a natural rewrite appears to require a new detail,
experience, source, or opinion, leave the detail out.

### Deflate wording without deleting the claim

Before:

> Northbridge Library opened in 1998. It has 12,000 books, runs a Saturday reading group, and hosts community meetings.
> Nestled in the heart of town, it stands as a vibrant testament to the community's enduring commitment to knowledge,
> showcasing the power of public spaces.

After:

> Northbridge Library opened in 1998 in the center of town. It has 12,000 books, runs a Saturday reading group, and
> hosts community meetings. Those activities demonstrate the community's enduring commitment to knowledge and the power
> of public spaces.

The promotional wording is formulaic, but it still carries claims about community commitment and public space. Do not
delete those claims merely because the excerpt does not show their evidence.

### Replace a vague participial tail

Before:

> The dashboard displays request latency, highlighting slow endpoints and providing teams with valuable visibility.

After:

> The dashboard displays request latency, highlights slow endpoints, and gives teams visibility into performance.

The repair converts vague appended analysis into direct actions without inventing new facts.

### Preservation case: unnamed attribution without a supplied source

Keep unchanged:

> Experts argue that the policy may improve retention.

If the surrounding source names the experts, name them. Otherwise de-AI editing alone does not authorize turning this
into the narrator's claim, deleting the uncertainty, or inventing a citation.

### Simplify filler without strengthening certainty

Before:

> At this point in time, it could potentially be argued that the system has the ability to reduce delays.

After:

> The system may reduce delays.

The shorter sentence keeps the epistemic qualification.

### Unpack formulaic rhetoric without losing its assertions

Before:

> Let's dive into CacheBox, a groundbreaking service that delivers speed, reliability, and scalability. It is not just a
> cache; it is the beating heart of the platform. The real question is whether teams can unlock its full potential.

After:

> CacheBox is a caching service that the source describes as a major advance. It is central to the platform and is
> intended to improve speed, reliability, and scalability. Teams still need to determine how fully they can use it.

The rewrite removes the helper voice, metaphor, negative pivot, and authority pose while preserving the assertions. If
`groundbreaking` is explicitly the author's supported judgment rather than sourced description, preserve that claim at
its proper strength instead of laundering it into fact.

### Remove assistant framing from a real tradeoff

Before:

> Here's how I'd think about the database choice. On one hand, PostgreSQL supports the extension the project needs. On
> the other hand, the team already operates MySQL. Ultimately, the right choice depends on whether extension support or
> operational familiarity matters more for this release.

After:

> PostgreSQL supports the extension the project needs, while the team already knows how to operate MySQL. For this
> release, the choice depends on whether extension support or operational familiarity matters more.

Do not invent a winner merely to avoid balanced phrasing.

### Describe the current system instead of the edit history

Before:

> This helper was added to replace the previous loop over every item. It now uses a hash map, which makes lookups faster.

After:

> The helper uses a hash map instead of scanning every item, which makes lookups faster.

Keep historical narration only when change history is actually the subject.

### Normalize detector-sensitive punctuation without flattening the sentence

Before:

> The first result looks promising—but the sample is small, and the authors call the effect “preliminary.”

After:

> The first result looks promising, but the sample is small, and the authors call the effect "preliminary."

The semantic relation and quotation remain intact. This normalization is a downstream presentation choice, not evidence
that the original was machine-written. Preserve typographic punctuation when a publication or supplied style requires it.

### Preservation case: legitimate passive voice and uncertainty

Keep unchanged:

> The samples were stored at -80°C before analysis, and the effect may reflect batch variation.

The actor is irrelevant to the storage statement, and `may` carries epistemic meaning. Do not make the sentence active
or categorical merely to sound less formulaic.

### Preservation case: legitimate personal cadence

Keep unchanged:

> I missed the train again. Honestly, that was on me. The platform clock had been broken since Tuesday, and I knew it.

A candid aside and irregular rhythm fit the supplied voice. Changing them would flatten it without repairing a cluster.

### Preservation case: already direct and appropriately uncertain

Keep unchanged:

> The trial produced three million lines of generated code. Developers reacted differently, and the implications remain
> unclear.

Do not add first-person reaction, humor, conflict, or a dramatic conclusion merely to make the passage feel human.

## False positives

Do not flag prose solely because it is polished, coherent, formal, concise, grammatical, impersonal, or free of personal
detail. Do not flag passive voice, a common transition, a three-part list, a rhetorical question, a short sentence, a
long sentence, a repeated technical term, or conventional academic structure in isolation.

Em dashes and curly quotation marks receive detector-sensitive normalization above, but they remain valid human
punctuation and are not evidence of authorship. Likewise, a functional semicolon, colon, fragment, or repeated technical
term can be exactly right.

Look for repetition plus functional weakness. If an edit would erase a deliberate choice, reduce precision, change claim
strength, falsify the voice, or violate the genre, keep the original.
