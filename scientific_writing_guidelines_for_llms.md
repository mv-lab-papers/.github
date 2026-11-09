# Scientific Writing Guidelines for Language Models

> **Purpose:** Use these instructions when drafting, revising, or reviewing scientific manuscripts in English. The goal is technically accurate, readable academic prose—not text that merely sounds academic.
>
> **Priority:** Follow the target journal's requirements and the author's explicit instructions. Otherwise, apply the rules below. Preserve technical meaning, qualifications, numerical results, and citations. Never invent evidence.

## 1. Core principle: write for an informed human reader

Write as a knowledgeable researcher explaining a study to other researchers, including readers who are not specialists in every subfield mentioned. A sentence should communicate a clear point on its first reading. Academic writing does not need to be difficult to sound rigorous.

**Prefer:** concrete subjects, explicit verbs, familiar terminology, and a logical sequence of ideas.

**Avoid:** compressed claims, noun-heavy phrases, fashionable jargon, excessive qualifications, and sentences that sound like abstracts of abstracts.

A useful test: **Would a competent researcher outside this narrow specialty understand the sentence without having to decode its grammar?** If not, rewrite it. Keep necessary technical terms, but explain their role.

## 2. Sentence-level rules

1. **Make the main claim visible.** Place the subject and main verb early. Do not bury the conclusion between qualifications.
2. **Express one main idea per sentence.** Split a sentence when it mixes research scope, methodology, justification, and implications.
3. **Prefer natural verbs to abstract nouns.** Write “we evaluated how the model performs” rather than “an evaluation of model performance was conducted.”
4. **Name what acts and what changes.** Avoid empty subjects such as “this,” “it,” or “the approach” when the referent is unclear.
5. **Avoid unnecessary negation.** Describe what the paper does before listing what it does not do. State exclusions where they matter to the interpretation.
6. **Avoid unnecessary contrasts.** Do not use “neither … nor …” or “not X but Y” just to make simple scope statements sound sophisticated.
7. **Use technical terms when they add precision.** Define specialized concepts on first use if the intended audience may not know them. Do not replace standard terms with vague substitutes.
8. **Use short, direct sentences by default.** Aim for roughly 15–25 words when practical; this is a guideline, not a strict limit. Longer sentences are appropriate when the structure remains easy to follow.
9. **Use transitions only when they clarify logic.** “However,” “therefore,” and “in contrast” should reflect a real logical relationship, not just decorate the prose.
10. **Prefer explicit relationships.** Say why a method was selected, what it measures, or how it supports a conclusion instead of simply naming a technique.
11. **Minimize stacked modifiers and compound nouns.** Rewrite strings like “held-out empirical latency-distribution estimation framework” as a short explanation.
12. **Use parallel structure.** When comparing two methods or listing outcomes, use similar grammatical forms.
13. **Remove words that add no information.** Common examples: “it is important to note that,” “in order to,” “the fact that,” “it should be emphasized that.”
14. **Avoid unexplained abbreviations.** Introduce an acronym only when it recurs enough to help the reader.
15. **Do not confuse concision with compression.** Saving ten words is not useful if a reader must reread the sentence twice.

## 3. Paragraph-level rules

Each paragraph should have one clear purpose: introduce a problem, explain a choice, describe a procedure, report a result, or interpret a finding.

A typical paragraph should:

- Start with the point the reader needs to know.
- Provide the relevant evidence, method, or explanation.
- State the implication or connect logically to the next paragraph when useful.

Avoid paragraphs that jump among unrelated claims. Avoid strings of very short declarative sentences with no explanation, and avoid paragraphs made of one huge sentence. Do not force every paragraph into a rigid template.

## 4. Precision without unreadable overqualification

Scientific caution is essential. Express it plainly.

- Distinguish **observation** (“we observed”), **inference** (“these results suggest”), and **demonstrated conclusion** (“the experiment shows … under the tested conditions”).
- State the population, data, setup, and conditions relevant to a claim.
- Quantify findings where possible: values, uncertainty, baselines, sample sizes, and practical effect sizes.
- Avoid unjustified certainty (“proves,” “guarantees,” “always,” “never”) and unjustified vagueness (“may potentially possibly”).
- Put limitations near the claims they constrain, but do not begin every statement with a defensive disclaimer.
- Preserve meaningful distinctions such as empirical performance versus theoretical guarantees. Explain those distinctions in ordinary language.
- Report negative or inconclusive results clearly; do not disguise them with ornate phrasing.

## 5. Write methods so the reader can reconstruct the reasoning

For each important method, answer in a natural order:

1. What was done?
2. Why was it done?
3. What data or inputs were used?
4. What assumptions and settings matter?
5. What quantity was measured or compared?

Do not describe a procedure using only a method name. A method name may be useful, but the reader also needs to know its role in this experiment.

**Weak:** “Moving-block replay preserves short dependence.”

**Better:** “We replayed consecutive blocks of observations to retain short-range temporal dependencies in the evaluation data.”

**If the limitation matters:** “This approach retains dependencies within each block, although it does not preserve all long-range relationships.”

Do not claim that a technique “preserves” a property perfectly unless that claim is justified by the actual method and assumptions.

## 6. Present results before interpretation

When presenting an experiment, distinguish:

- **Experimental setup:** what was compared and under which conditions.
- **Result:** what the measurements show, preferably with numbers.
- **Interpretation:** why the result may have occurred and why it matters.
- **Limitation:** what cannot be concluded from this evidence.

Avoid claiming improvement without naming a baseline or metric. Avoid describing a result as “significant” unless statistical significance is actually established or the word is explicitly used in a non-statistical sense.

**Weak:** “The proposed approach demonstrates superior robustness under challenging scenarios.”

**Better:** “Under the tested delay conditions, the method produced lower position error than the PID baseline. The difference was largest when communication delays varied between trials.”

Add numerical values if they are available; do not invent them.

## 7. Avoid common AI-generated academic prose patterns

| Avoid | Prefer |
|---|---|
| “It is worth noting that…” | State the fact directly. |
| “This highlights the importance of…” | Explain the specific implication. |
| “A comprehensive investigation was conducted…” | “We evaluated…” and name what was tested. |
| “In the context of the aforementioned framework…” | Name the actual method or system. |
| “Leveraging the capabilities of…” | “Using…” when no further distinction is needed. |
| “The utilization of…” | “The use of…” or an active verb. |
| “A novel and robust paradigm…” | Describe the actual contribution and evidence. |
| “The results clearly demonstrate…” | “The results show…” with the scope of the claim. |
| “Notwithstanding the inherent limitations…” | State the limitation directly. |
| “Facilitates enhanced performance…” | State what improved and by how much. |

Do not ban a phrase mechanically when it is genuinely apt. The problem is **empty or unnatural wording**, not the mere presence of individual words.

## 8. Worked example: technical but unreadable prose

### Original

> We claim neither schedulability nor measurement-based probabilistic timing analysis guarantees: our target is a held-out empirical distribution. Moving-block replay preserves short dependence [10]; process restarts expose between-run state.

### Why it is difficult to read

- The first sentence opens with two highly specialized exclusions before telling the reader what the study actually evaluates.
- “Our target is a held-out empirical distribution” does not explain which quantity is being measured or why.
- “Short dependence” and “between-run state” are compressed labels rather than clear explanations.
- The methods are named without explicitly showing their roles.
- A colon and semicolon force several different claims into a small space.

### Clearer version (assuming this reflects the actual method)

> Our study evaluates how well the method estimates the distribution of execution times on held-out data. We do not provide formal schedulability guarantees or probabilistic worst-case timing guarantees. To account for dependencies between nearby observations, we replay consecutive blocks of measurements [10]. We also restart the process between runs to examine whether its internal state affects the results.

**Important:** This rewrite illustrates style; it is not a factual validation of the methodology. Check whether “execution times,” “probabilistic worst-case timing guarantees,” “consecutive blocks,” and “internal state” match the actual paper. If the study uses another outcome or interpretation, replace those terms with the correct ones. Do not silently broaden or narrow a technical claim.

### Even more concise, if the detailed scope has already been established

> We evaluate the estimated timing distribution on held-out data rather than claim formal timing guarantees. The evaluation replays blocks of consecutive measurements to retain short-range dependencies [10] and restarts the process to assess differences between runs.

Use the shorter version only if the audience can already interpret the specialized terms.

## 9. More before-and-after examples

**Overcompressed:** “Cross-domain generalization remains contingent on distributional alignment.”

**Clear:** “The model may perform worse on data from a different domain, especially when the new data differ substantially from the training data.”

**Overabstract:** “Performance degradation is attributable to latency-induced state-estimation discrepancies.”

**Clear:** “Communication delays made the estimated position less accurate, which increased the final positioning error.”

**Artificially formal:** “A comparative assessment of the investigated architectures was undertaken.”

**Clear:** “We compared the architectures.”

**Ambiguous:** “This was found to be better under these conditions.”

**Clear:** “MPC produced lower position error than PID when the camera delay varied.”

**Misleading certainty:** “The proposed model is robust to changes in the data distribution.”

**More defensible:** “The model maintained similar accuracy across the three tested datasets. We did not evaluate larger distribution shifts.”

The alternatives are illustrative. Use them only when their factual content matches the research.

## 10. Discipline-specific terms and audience

Do not oversimplify established scientific concepts. Use terms such as “cross-validation,” “confidence interval,” “Monte Carlo simulation,” “moving-block bootstrap,” or “schedulability analysis” when they are technically correct and relevant. However:

- Explain what the method contributes to this particular study.
- Distinguish methods with similar names; never substitute a more familiar term for a different technique.
- When addressing a broad engineering audience, define niche terms on first use.
- Do not repeatedly define common terms for a specialist audience.
- Prefer a short explanatory sentence over a dense parenthetical definition.

## 11. Citations, equations, and claims

- Attach citations to the precise claims they support.
- Do not invent references, author names, results, or citation numbers.
- Do not treat a citation as a replacement for explaining the method.
- Define symbols at first use and maintain consistent notation.
- Explain the purpose and interpretation of important equations in prose.
- Do not restate every equation in words if it adds no value.
- Preserve all numerical values, units, conditions, uncertainty estimates, and cited support during editing.
- If information is missing, flag it for the author instead of filling it with plausible-sounding facts.

## 12. Editing workflow for a language model

When given a draft, follow this sequence:

1. **Identify the intended claim.** Determine what each sentence is trying to communicate and which constraints are essential.
2. **Check technical meaning.** Identify terms that cannot be safely paraphrased without domain knowledge.
3. **Rewrite for natural flow.** Put the central point first; use concrete subjects and verbs; unpack compressed claims.
4. **Preserve evidence and scope.** Keep all technical distinctions, conditions, data, quantities, citations, and uncertainty intact.
5. **Check continuity.** Make sure each sentence follows logically from the preceding one and each paragraph has a clear purpose.
6. **Read as a reviewer.** Ask: Could an expert who did not write this paper understand it in one reading? Would they know exactly what was tested and claimed?
7. **Remove artificial academic style.** Delete ornamental transitions, inflated vocabulary, repeated hedges, and unnecessary nominalizations.
8. **Flag uncertainty.** If a clearer rewrite requires assumptions about the experiment, ask the author or mark the uncertain phrase instead of inventing details.

Do not change the technical claims just to make the manuscript sound more confident or interesting.

## 13. Final self-check before producing text

Before returning a manuscript section, verify:

- [ ] The main claim of each sentence is identifiable on the first reading.
- [ ] An informed reader can follow the logic without decoding compressed terminology.
- [ ] Specialist terms are used accurately and explained where necessary.
- [ ] The scope and limitations are clear but not needlessly defensive.
- [ ] Methods are described by what they do, not only by their names.
- [ ] Claims follow from the actual evidence and quantitative results.
- [ ] No facts, metrics, assumptions, or citations were invented.
- [ ] The text sounds like a careful human researcher, not a language model imitating academic writing.

## 14. Ready-to-use instruction for an AI writing assistant

> Write clear, natural, technically precise scientific English. Prioritize communication over academic-sounding complexity. Put the main point first, prefer concrete subjects and active verbs, and explain the role of specialized methods rather than merely naming them. Avoid overcompressed claims, excessive nominalizations, defensive opening clauses, jargon stacking, semicolon-heavy sentences, and formulaic AI phrases. Keep all claims appropriately qualified, but state limitations plainly and only when relevant. Preserve technical distinctions, citations, numbers, and experimental conditions. Never invent evidence or silently change the meaning. If a sentence would require a knowledgeable reader to reread it, rewrite it more clearly, even if the result is longer.
