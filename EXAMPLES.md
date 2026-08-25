# Representative synthetic examples

These short examples are fictional, contain no patient data, and are not presented as validated
pharmacovigilance decisions.

The transcript blockquotes in Examples 1 and 2 are exact excerpts from the historical
MIT-licensed v1 synthetic corpus. The surrounding new or revised commentary has a separate
rights status. See [Rights and permitted use](RIGHTS.md) and the
[scoped historical MIT notice](HISTORICAL_V1_MIT_NOTICE.md).

## 1. Information buried inside an operational call

> «Και μια φαγούρα φοβερή με έπιασε από τότε που άρχισα αυτά τα χάπια, αλλά τέλος πάντων,
> την παράδοση να κανονίσουμε.»

The operational topic is delivery, but the caller also describes a symptom after starting a
product. Safety Net should surface the exact sentence for qualified human review. It should not
state that an adverse event has been confirmed.

## 2. Possible medication error

> «Σήμερα το πρωί του έδωσα διπλή δόση. Μπερδεύτηκα με τη θήκη της εβδομάδας.»

The screening layer can route this as a possible medication-error finding, identify missing
information, and present only closed, author-approved follow-up-question types. A qualified person
decides the next action.

## 3. Human-only or category disagreement

A separate author-defined synthetic registry record may identify a category even when the first
screening pass produces no corresponding finding, or it may use a different category. The model
output and the synthetic record remain visible as offline model/taxonomy-QA evidence; absence of a
model finding is not treated as evidence that the call is safe.

The approved product boundary does not add a frontline Adjudication page or a post-hoc diagnostic
model explanation. After independent judgments are frozen, a human-led offline comparison can
classify the disagreement as model error, author-label error, ambiguity, taxonomy mismatch,
insufficient information, or workflow disagreement.
