# English de-AI examples

Use these examples to calibrate transformations, not as phrases or topics to copy. Every rewrite must stay within the
facts, claims, uncertainty, and voice supplied by the input. If a natural rewrite appears to require a new detail,
experience, source, or opinion, leave the detail out.

## Deflate wording without deleting the claim

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

## Replace a vague participial tail

Before:

> The dashboard displays request latency, highlighting slow endpoints and providing teams with valuable visibility.

After:

> The dashboard displays request latency, highlights slow endpoints, and gives teams visibility into performance.

The repair converts vague appended analysis into direct actions without inventing new facts.

## Preserve unnamed attribution when no source is supplied

Before:

> Experts argue that the policy may improve retention.

After:

> Experts argue that the policy may improve retention.

If the surrounding source names the experts, name them. Otherwise de-AI editing alone does not authorize turning this
into the narrator's claim, deleting the uncertainty, or inventing a citation.

## Simplify filler without strengthening certainty

Before:

> At this point in time, it could potentially be argued that the system has the ability to reduce delays.

After:

> The system may reduce delays.

The shorter sentence keeps the epistemic qualification.

## Unpack formulaic rhetoric without losing its assertions

Before:

> Let's dive into CacheBox, a groundbreaking service that delivers speed, reliability, and scalability. It is not just a
> cache; it is the beating heart of the platform. The real question is whether teams can unlock its full potential.

After:

> CacheBox is a caching service that the source describes as a major advance. It is central to the platform and is
> intended to improve speed, reliability, and scalability. Teams still need to determine how fully they can use it.

The rewrite removes the helper voice, metaphor, negative pivot, and authority pose while preserving the assertions. If
`groundbreaking` is explicitly the author's supported judgment rather than sourced description, preserve that claim at
its proper strength instead of laundering it into fact.

## Remove assistant framing from a real tradeoff

Before:

> Here's how I'd think about the database choice. On one hand, PostgreSQL supports the extension the project needs. On
> the other hand, the team already operates MySQL. Ultimately, the right choice depends on whether extension support or
> operational familiarity matters more for this release.

After:

> PostgreSQL supports the extension the project needs, while the team already knows how to operate MySQL. For this
> release, the choice depends on whether extension support or operational familiarity matters more.

Do not invent a winner merely to avoid balanced phrasing.

## Describe the current system instead of the edit history

Before:

> This helper was added to replace the previous loop over every item. It now uses a hash map, which makes lookups faster.

After:

> The helper uses a hash map instead of scanning every item, which makes lookups faster.

Keep historical narration only when change history is actually the subject.

## Normalize detector-sensitive punctuation without flattening the sentence

Before:

> The first result looks promising—but the sample is small, and the authors call the effect “preliminary.”

After:

> The first result looks promising, but the sample is small, and the authors call the effect "preliminary."

The semantic relation and quotation remain intact. This normalization is a downstream presentation choice, not evidence
that the original was machine-written. Preserve typographic punctuation when a publication or supplied style requires it.

## Preserve legitimate passive voice and uncertainty

Before:

> The samples were stored at -80°C before analysis, and the effect may reflect batch variation.

After:

> The samples were stored at -80°C before analysis, and the effect may reflect batch variation.

The actor is irrelevant to the storage statement, and `may` carries epistemic meaning. Do not make the sentence active
or categorical merely to sound less formulaic.

## Preserve legitimate personal cadence

Before:

> I missed the train again. Honestly, that was on me. The platform clock had been broken since Tuesday, and I knew it.

After:

> I missed the train again. Honestly, that was on me. The platform clock had been broken since Tuesday, and I knew it.

A candid aside and irregular rhythm fit the supplied voice. Changing them would flatten it without repairing a cluster.

## Do not manufacture personality

Before:

> The trial produced three million lines of generated code. Developers reacted differently, and the implications remain
> unclear.

After:

> The trial produced three million lines of generated code. Developers reacted differently, and the implications remain
> unclear.

The passage is already direct and appropriately uncertain. Do not add first-person reaction, humor, conflict, or a
dramatic conclusion merely to make it feel human.
