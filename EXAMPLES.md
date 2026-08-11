# Representative synthetic examples

These short examples illustrate the intended interaction. They are fictional, contain no patient
data, and are not presented as validated pharmacovigilance decisions.

## 1. Information buried inside an operational call

> «Και μια φαγούρα φοβερή με έπιασε από τότε που άρχισα αυτά τα χάπια, αλλά τέλος πάντων,
> την παράδοση να κανονίσουμε.»

The operational topic is delivery, but the caller also describes a symptom after starting a
product. Safety Net should surface the exact sentence for human review. It should not state that an
adverse event has been confirmed.

## 2. Possible medication error

> «Σήμερα το πρωί του έδωσα διπλή δόση. Μπερδεύτηκα με τη θήκη της εβδομάδας.»

The screening layer can route this as a possible medication-error finding, identify missing
information, and present only approved follow-up-question types. A person decides the next action.

## 3. Human-only disagreement

A pre-existing human or registry record may identify a category even when the first screening pass
produces no corresponding finding. The case stays visible as `human-only` and becomes a model-QA or
adjudication item; absence of a model finding is not treated as evidence that the call is safe.

A future diagnostic pass may explain why no finding was emitted — for example, ambiguous evidence,
a different category, an out-of-scope situation, or a possible model miss. That explanation cannot
dismiss or override the human record.
