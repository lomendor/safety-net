# Evaluation note

## Status

- Prototype evaluation / pre-validation
- Synthetic data only
- Expected labels created by the project author
- No independently validated ground truth

## Question tested

Can the prototype execute its intended screening-and-review mechanics on a frozen synthetic corpus
while grounding findings in exact transcript evidence and preserving disagreements?

The experiment does **not** test performance on real patient-support calls.

## Data packs

| Pack | Size | Purpose |
|---|---:|---|
| Demo | 15 calls plus one guided case | End-to-end workflow demonstration |
| Standard evaluation | 50 cases | Functional regression against frozen author labels |
| Challenge | 12 cases | Less obvious missed-signal patterns and negative controls |

The complete cases, expected labels, rationales, and model outputs are intentionally not published
in this showcase.

## Recorded baseline

The standard evaluation contained 25 author-labelled positives and 25 author-labelled negatives.
All 25 positives produced at least one expected-category finding, and none of the 25 negatives
produced a finding. Across that run, 73 of 73 evaluated evidence excerpts matched the transcript
verbatim.

The separate challenge contained eight deliberately difficult positives and four negative
controls. All eight positives produced findings, including two author-labelled seriousness
indications. One of four negative controls was also flagged, so the predeclared challenge gate
remained **FAIL**.

## Why the FAIL remains

The flagged negative-control case described a possible reaction involving another medicinal
product and information about a third person. Later review made the original negative label
uncertain. The label, prompt, and recorded run were not changed retrospectively.

The useful question is therefore not merely whether the model was "wrong", but whether the model,
the author label, the taxonomy, or the case construction caused the disagreement.

## Next valid experiment

An independent reviewer should initially receive 5–10 synthetic cases without author labels,
model outputs, rationales, or pack membership. For each case, the reviewer should record whether it
warrants human PV review, the possible issue type, possible seriousness indicators, follow-up needs,
and whether the case itself is ambiguous.

The comparison should preserve all three judgments:

`author label ↔ independent judgment ↔ Safety Net`

Disagreements should be classified as model error, author-label error, ambiguous case, taxonomy
mismatch, insufficient information, or workflow disagreement. A lower score with visible,
inspectable disagreements would be more informative than another self-authored perfect result.
