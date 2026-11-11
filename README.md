# Publication guidelines

These guidelines apply to every manuscript written in this organization's repositories, whether by a person or by a language model. They cover journal articles, conference papers and software papers in applied machine learning, signal processing, machine vision and related engineering fields.

The goal is clear, restrained, technically precise English that a researcher can understand on the first reading and reproduce.

## Order of priority

1. The target journal's or conference's requirements.
2. The authors' explicit instructions for the manuscript.
3. These guidelines.

Whatever the instructions say, never invent evidence, results, references, parameters or citations. If information is missing, flag it for the authors.

## Files

| File | Contents |
|---|---|
| [writing_guidelines.md](writing_guidelines.md) | Part I: style (sentences, paragraphs, terminology, abbreviations, hedging, phrases to avoid). Part II: paper structure (the Abstract through the Conclusion, contributions, limitations, figures, numbers) and the pre-submission checklist. |
| [mathematical_notation_guidelines.md](mathematical_notation_guidelines.md) | Equations, symbols, the notation register and the notation audit. |

## Core rules

1. **Write for an informed human reader.** A competent researcher outside the narrow specialty should understand each sentence on the first reading.
2. **One claim per sentence, one idea per paragraph.** The first sentence of a paragraph states what the paragraph establishes.
3. **Define every symbol at first use**, with its domain and units, in a `where …` clause right after the equation. Every displayed equation must do identifiable work.
4. **Justify every design choice and every number**: parameter values, epochs, thresholds, baselines and the split strategy.
5. **State contributions as things a reader can check.** Name the artifact, the comparison and the condition, not a quality such as "novel" or "powerful".
6. **Match the verb to the evidence.** Use *show* for measured results with spread, *indicate* or *suggest* for indirect evidence, *may* for untested explanations, and *prove* only for mathematics.
7. **Report spread and protocol with every headline number**: mean ± SD or a confidence interval, the number of runs or folds, and the unit the data were split by.
8. **Report negative and null results** in the same plain register as positive ones.
9. **Keep each section to its job.** Do not interpret in Methods, do not report new data in the Discussion, and do not add new background in the Conclusion.
10. **Use one term per concept and one meaning per symbol.**
11. **Use "we" consistently for the authors.**
12. **Delete any sentence that would fit unchanged into a paper on a different topic.**

## Before submission

Work through the [pre-submission checklist](writing_guidelines.md#28-pre-submission-checklist) and the [notation audit](mathematical_notation_guidelines.md#4-validate-after-drafting-and-after-every-mathematical-revision).

## For language models

Follow all of the above. In addition:

### Rules you must never break

- **Never invent** facts, results, numbers, parameters, datasets, references, author names or citation numbers.
- **Preserve** every technical claim, qualification, numerical value, unit, condition, uncertainty estimate and citation.
- **Do not change how strong a claim is** to make the text sound more confident or more interesting. Never silently broaden or narrow a technical claim.
- **Flag gaps instead of filling them.** If a clearer rewrite needs an assumption about the experiment, ask the authors or mark the passage, e.g. `[AUTHORS: confirm the split unit]`. Do not invent derivations, algorithms or event rules to make the notation audit pass.
- **Treat the rewrite examples in these guidelines as style illustrations, not facts.** Reuse their content only when it matches the research.

### Editing workflow

1. **Identify the intended claim** of each sentence and the constraints that are essential to it.
2. **Check the section's job** ([Part II](writing_guidelines.md#15-rules-that-span-the-whole-paper)). Move misplaced material, for example study aims found in Related Work or interpretation found in Results.
3. **Keep technical terms** that cannot be paraphrased safely without domain knowledge.
4. **Rewrite for flow.** Put the main point first, use concrete subjects and verbs, unpack compressed claims, and aim for 15–25 words per sentence.
5. **Calibrate certainty** ([§10](writing_guidelines.md#10-hedging-and-scientific-uncertainty)) and keep evidence and scope intact.
6. **Unify terms and voice.** Use one term per concept and "we" for the authors. Check pronouns in context rather than with find-and-replace.
7. **Remove artificial style**: the phrases in [§11](writing_guidelines.md#11-generic-ai-sounding-expressions) and [§12](writing_guidelines.md#12-unnecessary-jargon-and-wordiness), ornamental transitions and nominalizations.
8. **Audit the mathematics** with the [notation audit](mathematical_notation_guidelines.md#4-validate-after-drafting-and-after-every-mathematical-revision).
9. **Read as a reviewer.** Would an expert who did not write the paper know exactly what was tested and what is claimed?
10. **Report** every item you flagged or could not resolve, with its location.

When asked to **review** rather than edit, report each issue with its location, the rule it breaks and a proposed fix. Separate substantive issues (unsupported claims, missing protocol details, leakage, undefined symbols, unanswered aims) from stylistic ones. Do not present a stylistic preference as an error when the text is already clear.

### Ready-to-use instruction

> Write clear, restrained, technically precise scientific English for an informed researcher. Put the main point first, with one claim per sentence and one idea per paragraph. Prefer concrete subjects and verbs. Use "we" for the authors, with the active voice for decisions and the passive voice for routine procedure. Explain what each method does in this study and why each parameter value was chosen. Define every symbol at first use, with its domain. Use one term per concept. Match the verb to the evidence: "shows" for measured results with spread, "suggests" for indirect evidence, "may" for untested explanations. Report numbers with uncertainty, run counts and a named baseline, and state null results plainly. Keep each section to its job. Avoid formulaic AI phrases (crucial role, leverage, comprehensive, novel, paves the way, it is worth noting), wordy jargon, stacked hedges and semicolon-heavy sentences. Preserve all technical claims, numbers, conditions and citations. Never invent evidence; flag missing information instead. If a sentence would make a knowledgeable reader reread it, rewrite it more clearly, even if it becomes longer.
