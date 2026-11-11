# Writing guidelines

This file holds the writing rules for the [publication guidelines](README.md). Part I covers how to write: sentences, paragraphs, terminology, argument and caution. Part II covers what each part of a paper contains. Equations are covered separately, in [mathematical_notation_guidelines.md](mathematical_notation_guidelines.md).

If the venue prescribes a different section order (for example, Results before Methods), follow the venue but keep the content rules.

# Part I — Style

## 1. Core principle: write for an informed human reader

Write as a researcher explaining a study to other researchers, including readers who are not specialists in every subfield the paper touches. Each sentence should make its point on the first reading. Rigorous writing does not need to be difficult.

- **Prefer** concrete subjects, explicit verbs, familiar terminology and a logical order of ideas.
- **Avoid** compressed claims, noun-heavy phrases, fashionable jargon, stacked qualifications and sentences that read like an abstract of an abstract.

**Test:** Would a competent researcher outside this specialty understand the sentence without decoding its grammar? If not, rewrite it. Keep the necessary technical terms, but make their role clear.

## 2. Authorial voice, tense and grammatical voice

### 2.1 Person

- Refer to the authors with the first-person plural (**we, us, our**) and plural verb agreement, everywhere: abstract, main text, captions, appendices and supplementary material.
- Do not switch to "I" or "my". Do not call yourselves "the authors", and never address the reader as "you".
- Keep the original person inside verbatim quotations and attributed participant statements.
- Sentences with other subjects ("the model predicts …") are fine. The rule only governs how the authors refer to themselves.
- When revising, check pronouns and verb agreement in context. Do not run a blind find-and-replace.

### 2.2 Active and passive voice

- **Use the active voice for decisions and for anything with consequences:** "We split the data by subject so that …".
- **Use the passive voice for routine procedure** where who did it does not matter: "Images were resized to 512 × 512 px."
- Do not use the passive to hide responsibility for a choice.

### 2.3 Tense

- **Use the present tense** for what the paper contains, for general facts and for what figures and tables show: "Table 3 lists …", "The filter output is given by (4)."
- **Use the past tense** for what was done and found: "The model was trained for 150 epochs." "The error decreased by 12 %."

## 3. Sentences

1. **Make the main claim visible.** Put the subject and main verb early, and move conditions and citations to the end. Do not bury the conclusion between qualifications.
2. **Express one main idea per sentence.** Split any sentence that mixes scope, method, justification and implication.
3. **Aim for 15–25 words.** Split anything over about 35 words unless it is a list or its structure stays easy to follow. This is a guideline, not a hard limit.
4. **Prefer verbs to abstract nouns.** Write "we evaluated how the model performs", not "an evaluation of model performance was conducted".
5. **Name what acts and what changes.** Avoid "this", "it" or "the approach" when the referent is unclear.
6. **Avoid unnecessary negation.** Say what the paper does before what it does not do. A scope sentence ("The goal is not X, but Y") is useful once, where it stops readers judging the paper against a goal it never had (see [§9.2](#92-argument-shapes-that-work)). Do not use "neither … nor" or "not X but Y" elsewhere just to sound sophisticated.
7. **Avoid stacked modifiers and compound nouns.** Rewrite a phrase like "held-out empirical latency-distribution estimation framework" as a short explanation.
8. **Use parallel structure** when comparing methods or listing outcomes.
9. **Use one type of number per sentence where possible.** Mixing percentages, absolute counts and ratios in one sentence slows the reader down.
10. **Remove words that add no information** (see [§11](#11-generic-ai-sounding-expressions) and [§12](#12-unnecessary-jargon-and-wordiness)).
11. **Do not confuse concision with compression.** Saving ten words is pointless if the reader has to read the sentence twice. When unsure, choose the clearer and longer version.

| Do | Avoid |
|---|---|
| The data were split by subject, so that recordings of one subject never appear in both training and test sets. | In order to make sure that there is no data leakage, which could otherwise be a problem, the splitting of the data was done in such a way that it was done on the level of subjects. |
| We set the filter length to *n* = 8; longer filters did not reduce the validation error and increased run time. | The filter length was chosen experimentally. |

## 4. Paragraphs

- **Each paragraph has one purpose**: to introduce a problem, explain a choice, describe a procedure, report a result or interpret a finding.
- **Start with a topic sentence** that states the point. The rest of the paragraph supports, qualifies or quantifies it.
- **Keep paragraphs to 3–7 sentences.** A one-sentence paragraph is acceptable only for a transition or a key result.
- **End on the consequence** or on a logical link to the next paragraph, not on a new topic.
- **Do not restate a paragraph's message** in consecutive sentences with different wording. This happens most often at the end of literature reviews. Keep the sharper sentence.
- **Avoid strings of short declarative sentences with no explanation**, and avoid paragraphs made of one very long sentence.
- **Never paste the same paragraph twice.** Search for near-duplicates after merging drafts from several authors.
- Do not force every paragraph into one rigid template.

## 5. Lists

- Use bulleted lists for **contributions, assumptions, limitations and procedural steps**. Write arguments as prose.
- Keep list items **grammatically parallel**: all noun phrases or all full sentences, all in the same tense.
- Use numbered steps for an algorithm only if it cannot be shown as an `Algorithm` block or pseudocode.

## 6. Terminology

- **Use one term for one concept.** Do not alternate between synonyms for variety. If you write "flower cluster", do not later write "flower set", and if you write "dataset", do not switch to "data set".
- **Use standard names for standard things**, for example "10-fold cross-validation repeated 10 times", "leave-p-out cross-validation (p = 3)", "Cohen's *d*" and "global average pooling".
- **Define a term you coin once, in one sentence, and keep it fixed.** This applies to a descriptor, an annotation type or a label source, for example. If there are several related terms, a small comparison table is clearer than scattered descriptions.
- **Use precise quantities instead of adjectives**: "1,450 training images" rather than "a large dataset", and "10 s segments" rather than "short segments".
- **Do not oversimplify established concepts.** Use terms such as "confidence interval", "Monte Carlo simulation" or "moving-block bootstrap" when they are correct. However:
  - say what the method contributes to *this* study;
  - distinguish methods with similar names, and never substitute a more familiar term for a different technique;
  - define niche terms at first use when writing for a broad engineering audience, but do not define common terms over and over for specialists;
  - prefer a short explanatory sentence to a dense parenthetical definition.

## 7. Abbreviations

- Spell out every abbreviation at first use, followed by the abbreviation in parentheses, e.g. "electrocardiogram (ECG)". Use only the abbreviation after that.
- The abstract and the main text are separate. Define an abbreviation again at its first use in the main text, even if the abstract already defined it.
- Do not abbreviate a term that appears fewer than three times. Write it out each time.
- Do not use abbreviations in the title or in section headings.
- Captions must stand alone, so define any abbreviation a caption uses within that caption.

## 8. Precision

- Distinguish **observation** ("we observed"), **inference** ("these results suggest") and **demonstrated conclusion** ("the experiment shows … under the tested conditions").
- State the population, data, setup and conditions that a claim depends on.
- Quantify findings: give values, uncertainty, baselines, sample sizes and practical effect sizes.
- Keep distinctions that matter, such as empirical performance versus theoretical guarantees, and explain them in plain language.
- Do not claim that a technique "preserves" or "guarantees" a property unless the method and its assumptions justify it.

## 9. Transitions and argumentation

### 9.1 Connectors

Use a connector only when it states a real logical relation, and choose the one that matches the relation:

| Relation | Use | Avoid |
|---|---|---|
| consequence | therefore, so, thus | "Therefore, … Hence, … Thus, …" in consecutive sentences |
| contrast | however, but, in contrast, whereas | opening every second sentence with "However," |
| addition | also, in addition | "Moreover, … Furthermore, … Additionally, …" chains |
| concession | although, while | |
| specification | in particular, specifically, for example | |

If a paragraph needs a connector on every sentence, the sentences are in the wrong order.

### 9.2 Argument shapes that work

- **Gap → consequence → response.** Say what existing methods do, what they cannot do, why that matters here, and what this paper does instead.
- **Assumption → test.** State the assumptions explicitly, in a bulleted list if there are several, then show the measurement that supports or weakens each one.
- **Expected vs. observed.** For a surprising result, say what was expected, what was observed, and the most likely reason, marked as a hypothesis.
- **Scope sentence.** State once what the paper does *not* try to do, for example: "The goal is not to maximize accuracy, but to test whether …".
- **Explicit relationships.** Say why a method was chosen, what it measures and how it supports the conclusion. Naming a technique is not enough.

### 9.3 Argument shapes to avoid

- **Importance by assertion**, as in "This area is important and requires further focus." Show importance with a cost, a risk, a count or a failure mode.
- **Causal claims from correlation**, as in "Because the values are similar, the device has no influence." Write instead: "We found no difference larger than X between devices."
- **Generalizing from one setup**, as in "Model A is well suited for this task." Write instead: "Model A ranked highest on both datasets we tested."
- **Shaping the literature** so that the chosen method looks necessary.

## 10. Hedging and scientific uncertainty

### 10.1 Calibrate the verb to the evidence

| Evidence | Verb |
|---|---|
| Mathematical derivation | proves, follows from |
| Repeated measurements with reported spread and effect size | shows, demonstrates |
| A single run, a small sample, a proxy metric, or visual inspection | indicates, suggests |
| An explanation not tested in the paper | may, might, could, one possible reason is |
| Speculation about other domains | we expect, it remains to be tested whether |

### 10.2 Rules

- **Hedge once, in the right place.** Avoid stacked hedges such as "it might possibly suggest that it could".
- **Do not hedge measured facts.** "The MAE was 2.1 ± 0.2" needs no "approximately".
- **Do not overstate certainty** with "proves", "guarantees", "always" or "never" for empirical findings.
- **Use "significant" only for statistical significance.** Otherwise write "substantially" or give the number.
- **Do not use "clearly" or "obviously"** about your own results. If a result is clear, the number shows it.
- **Attach the sample size to claims based on small groups**, as in "With only seven subjects in this group, the result is preliminary."
- **Avoid hope language** such as "give hope" or "promising" without a number. Say what would need to be tested next.
- **Place each limitation next to the claim it constrains**, but do not open every statement with a defensive disclaimer.
- **Report negative or inconclusive results plainly**, without ornate phrasing.

| Do | Avoid |
|---|---|
| Accuracy differed by less than 0.5 percentage points between the two sensors (Table 5), which suggests that the choice of sensor had little effect in this dataset. | According to this finding it is possible to conclude that the sensor does not influence the results. |
| The model maintained similar accuracy across the three tested datasets. We did not evaluate larger distribution shifts. | The proposed model is robust to changes in the data distribution. |

## 11. Generic AI-sounding expressions

The phrases below carry no information or make the text read as machine-generated. Delete them, or replace them with the specific fact. Do not ban a word mechanically when it is genuinely apt; the problem is empty or unnatural wording.

| Avoid | Prefer |
|---|---|
| delve into, dive into | examine, analyze, or just state the analysis |
| plays a crucial / pivotal / vital role | the actual dependency: "determines", "limits", "accounts for X %" |
| in today's world, in recent years X has gained significant attention | start with the problem |
| a formidable / pressing challenge | what makes it hard |
| leverage, harness, utilize, the utilization of | use |
| robust, powerful, seamless, cutting-edge (unquantified) | the measured property |
| a comprehensive investigation / evaluation was conducted | "We evaluated …" and say what was tested |
| a novel and robust paradigm | the actual contribution and its evidence |
| paves the way, opens new avenues, sheds light on | the concrete next step |
| a testament to, underscores, this highlights the importance of | the specific implication |
| intricate, multifaceted, nuanced | the specific complications |
| valuable insights, valuable resource | the insight or the use |
| landscape, realm, paradigm, ecosystem | field, setting, approach |
| in the context of the aforementioned framework | name the method or system |
| facilitates enhanced performance | what improved, and by how much |
| the results clearly demonstrate | "the results show …" with the scope of the claim |
| notwithstanding the inherent limitations | state the limitation |
| it is worth noting that, it is important to highlight that | state the fact |
| not only … but also (as a habit) | and |
| "In summary," / "Overall," at the start of paragraphs | use once, at the end of a section |
| triplets of adjectives ("simple, robust, and efficient") | one adjective with its evidence |
| frequent em-dashes and semicolons that pack several claims into one sentence | separate sentences |

## 12. Unnecessary jargon and wordiness

| Wordy | Plain |
|---|---|
| in order to | to |
| it is possible to + verb | can + verb |
| due to the fact that, the fact that | because, that |
| a number of / a large number of | several, many, or the number |
| with respect to, in terms of (as filler) | for, in |
| the aforementioned, the above-mentioned | this, these, or the name |
| it should be emphasized that | (delete) |
| methodology (meaning a method) | method |
| functionality | function, feature |
| performs the computation of | computes |
| is able to | can |
| prior to | before |
| has the potential to | can, may |
| the proposed X (in every sentence) | name it once, then use the name |

## 13. Before-and-after examples

These rewrites illustrate style only. Use one only when its factual content matches the research.

| Problem | Before | After |
|---|---|---|
| Overcompressed | Cross-domain generalization remains contingent on distributional alignment. | The model may perform worse on data from another domain, especially when the new data differ substantially from the training data. |
| Overabstract | Performance degradation is attributable to latency-induced state-estimation discrepancies. | Communication delays made the estimated position less accurate, which increased the final positioning error. |
| Artificially formal | A comparative assessment of the investigated architectures was undertaken. | We compared the architectures. |
| Ambiguous | This was found to be better under these conditions. | MPC produced lower position error than PID when the camera delay varied. |
| Method named, role missing | Moving-block replay preserves short dependence. | We replayed consecutive blocks of observations to retain short-range temporal dependencies in the evaluation data. This retains dependencies within each block but not all long-range relationships. |
| Unscoped improvement | The proposed approach demonstrates superior robustness under challenging scenarios. | Under the tested delay conditions, the method produced lower position error than the PID baseline. The difference was largest when delays varied between trials. |

### Worked example: technical but unreadable

> **Original:** We claim neither schedulability nor measurement-based probabilistic timing analysis guarantees: our target is a held-out empirical distribution. Moving-block replay preserves short dependence [10]; process restarts expose between-run state.

**Why it is hard to read:**

- It opens with two specialized exclusions before saying what the study evaluates.
- It never says which quantity is measured.
- "Short dependence" and "between-run state" are compressed labels, not explanations.
- It names methods without saying what they do here.
- A colon and a semicolon force four claims into two sentences.

> **Clearer** (assuming this matches the actual method): Our study evaluates how well the method estimates the distribution of execution times on held-out data. We do not provide formal schedulability guarantees or probabilistic worst-case timing guarantees. To account for dependencies between nearby observations, we replay consecutive blocks of measurements [10]. We also restart the process between runs to examine whether its internal state affects the results.

> **Shorter**, if the readers already know the terms: We evaluate the estimated timing distribution on held-out data rather than claim formal timing guarantees. The evaluation replays blocks of consecutive measurements to retain short-range dependencies [10] and restarts the process to assess differences between runs.

Check that terms such as "execution times" and "internal state" match the actual paper. Never silently broaden or narrow a technical claim.

## 14. Common language errors

Check for these before submission. Several are typical of authors whose first language has no articles.

- **Articles.** Write "*The* error of *the* filter is shown in *the* figure", not "Error of filter is shown in figure". Check a/an at first mention and "the" afterwards.
- **Spelling in headings and captions** ("Discussion", not "Discusion"). Spell-checkers often skip headings, captions and table cells.
- **Homophones and near-misses:** weakly / weekly, lighting / lightning, effect / affect, then / than, principal / principle.
- **Calques:** "Example follows:" should be "For example:"; "analogically" should be "analogously"; "can be understand" should be "can be understood".
- **Leftover draft material:** notes in another language, placeholder citations, editor comments. Search for brackets, "TODO" and non-English words.
- **Duplicated paragraphs** after merging text from co-authors.
- **Wrong figure and table numbers** after reordering.
- **Undefined abbreviations in captions.**

---

# Part II — Paper structure

## 15. Rules that span the whole paper

- **Each section does one job.**
  - The Introduction motivates the work and states its aim.
  - Related Work positions the paper in the literature.
  - Methods enable reproduction.
  - Results report.
  - The Discussion interprets.
  - The Conclusion summarizes.
- **Keep reporting and interpretation apart.** Results report what was measured, and the Discussion explains it.
- **Answer every aim.** Every aim or research question stated in the Introduction is explicitly answered in the Discussion or the Conclusion.
- **Keep terms and notation consistent** across all sections, captions and appendices.

## 16. Title

- Name the problem and the approach in concrete terms.
- Do not use abbreviations.
- Avoid claims such as "novel", "efficient" or "robust" in the title.

## 17. Abstract (150–250 words)

The abstract covers the following topics in this order, roughly one sentence each, whether it is structured (with headings) or a single paragraph:

1. **Problem** and why it matters, stated concretely.
2. **Gap:** what existing methods lack.
3. **Aim or approach:** what this paper proposes, in one sentence without adjectives.
4. **Methods:** data and protocol, including size, source and validation scheme.
5. **Results:** the main quantitative result, including the comparison. Give at least one number, such as an effect size, an error with its spread, or a p-value.
6. **Implication:** one sentence, with its scope stated.

Do not use citations, references to figures or tables, or undefined abbreviations. Do not end with a sweeping statement about "the field". An abstract that contains only motivation and no numbers is not finished.

## 18. Introduction

**Purpose:** to take the reader from the application problem to the specific gap and to this paper's response.

1. **Context (one paragraph).** Name the application and a concrete stake: a cost, a risk, a manual effort or a failure mode. Cite a source for every statistic.
2. **Technical difficulty (one or two paragraphs).** Explain why the problem is hard *for the data at hand*, for example because of non-stationarity, occlusion, scarce labels, offsets or class imbalance.
3. **Gap (one paragraph).** Say what current approaches cannot do, with citations. The detailed review belongs in Related Work if the paper has that section.
4. **Aim and contributions (last paragraph).** State the aim of the paper and give the bulleted contribution list (see [§19](#19-contributions)).
5. **Scope sentence (recommended).** Say what the paper does not attempt.
6. **Roadmap (optional).** Use one sentence, and only when the structure departs from the venue's standard.

Do not open with "In recent years, X has gained significant attention". Do not write a history going back decades, and do not write more than one paragraph of motivation without a citation.

## 19. Contributions

- Place the contribution list at the **end of the Introduction**, with two to four items.
- Each item names **what** is new, **relative to what**, and **where** in the paper it is shown.
- Distinguish the kinds of contribution: a method, a dataset, an evaluation protocol, a software artifact or an empirical finding. Do not list one artifact as three contributions.
- If the paper extends earlier work by the same authors, **state exactly what differs**: new data, a new population, a new device or a new comparison.
- Do not write "completely new", "unique", "first" or "pioneering" unless you have checked the claim and cite the closest prior work in the same sentence. "To our knowledge, no prior study has evaluated X under condition Y" is acceptable when the closest related work follows it.

| Do | Avoid |
|---|---|
| We release a dataset of 900 annotated images from three sites, with manually verified labels for every sample (Section 3.1). | We present a valuable resource that will benefit researchers and practitioners. |
| We propose a classifier trained only on image-level labels; Section 4 compares it with a detection baseline and a fully supervised baseline on the same split. | We propose a novel, powerful and robust framework that significantly outperforms state-of-the-art methods. |
| Compared with our earlier conference version, this study adds an independent test group recorded with a second sensor. | This study is an extension of previous work. |

## 20. Related Work

**Purpose:** to synthesize prior research and position this paper within it. It is not a catalogue of papers.

- **Group work by approach**, for example "detection-based counting" versus "regression-based counting", with one subsection or paragraph per group. Organize the section around how the field developed and what each line of work can and cannot do.
- **Synthesize before citing.** Start each group with what its methods have in common, then cite examples.
- **Vary the subject of the sentences.** Do not open twelve sentences with "In [n], the authors …". Make the method or the finding the subject.
- **Quote numbers from other papers only when they are comparable**, meaning the same task and the same metric. Otherwise, say why they cannot be compared.
- **End each group with the limitation that matters for this problem**, supported by the cited literature.
- **Close with a short positioning paragraph** that states how this paper differs from the closest prior work, at the level of the gap: what is missing, and which kind of approach this paper takes.
- **Keep the present study's details out of this section.** Its aims and contribution list go in the Introduction. Its method, datasets, parameter choices, experimental design and evaluation procedure go in Methods. Describing a *cited* study's method is fine when it helps comparison.
- **Do not shape the literature** to make the chosen method look necessary.
- **State any deliberate omissions**, for example: "We restrict the review to methods that require no object-level labels."

| Do | Avoid |
|---|---|
| Detection-based counters estimate the number of *visible* objects; they need box or polygon labels and miss occluded instances [12–15]. Reported precision ranges from 0.7 to 0.95, but each study defines its own dataset and visibility criterion, so the figures are not directly comparable. | In [12] the authors used Faster R-CNN. In [13] the authors used Mask R-CNN. In [14] the authors used YOLOv3. In [15] the authors used YOLOv5. |

## 21. Methods

**Purpose:** to let a competent reader reproduce the work and judge whether the comparison is fair.

### 21.1 Structure

1. **Overview.** One paragraph that maps the pipeline onto the subsections. Add a pipeline figure if there are more than three stages.
2. **Data.** Source, acquisition, labels and label quality, inclusion and exclusion criteria, the split, and leakage control. If labels come from several sources, compare them in a table.
3. **Method.** Equations with full symbol definitions (see the [notation guide](mathematical_notation_guidelines.md)). Describe the architecture in the order data flows through it. Keep textbook components (ResNet, NLMS, SVM and similar) to two to four sentences with a citation, and spend the space on what you changed.
4. **Baselines.** Say why each baseline was chosen, how it was implemented and tuned, and confirm that it received tuning effort comparable to the proposed method.
5. **Protocol.** The cross-validation scheme, number of repetitions, seed policy, stopping criterion, metrics with their definitions, hardware and software.

### 21.2 For each important step, answer five questions

1. What was done?
2. Why was it done?
3. What data or inputs were used?
4. What assumptions and settings matter?
5. What quantity was measured or compared?

A method name is not a description. Say what the method does in this experiment.

| Do | Avoid |
|---|---|
| We replayed consecutive blocks of observations to retain short-range temporal dependencies in the evaluation data. | Moving-block replay preserves short dependence. |
| … for 150 epochs, because the validation error stopped improving after about 120 epochs. | … for 150 epochs. |

### 21.3 Reproducibility facts

Report each of the following, or state that it does not apply:

- the data source, acquisition device and resolution, the count per class, and the inclusion and exclusion criteria;
- the **unit the data were split by** (subject, tree, engine, source image), and **why that unit prevents leakage**;
- the preprocessing steps, in the order they were applied;
- model size (parameters, and FLOPs where relevant);
- the optimizer, learning-rate schedule, epochs and batch size, with **the reason** for each value;
- the number of repeated runs and the seed policy;
- hardware, operating system and library versions;
- where the data and code are available.

### 21.4 Avoid

- "Chosen experimentally" without stating the criterion.
- Hyperparameters "left at default" without giving the library version.
- Results or interpretation in Methods. The one exception is an empirical justification of a parameter value.
- Deriving the same equation again in several sections.

## 22. Results

**Purpose:** to report what was measured, most important first.

- **Separate the setup, the result and the interpretation.** Results states what was compared, under which conditions, and what was measured. Keep interpretation to a single clause ("…, which indicates …"). Longer explanations belong in the Discussion.
- **Open each subsection with the main comparison**, then the exceptions, then secondary analyses such as ablations, timing and per-group breakdowns.
- **Point to the table or figure, then state the finding in words.** "Results are in Table 4" alone is not enough.
- **Name the baseline and the metric** in every claim of improvement.
- **Report mean ± SD or a confidence interval**, the number of runs, and an effect size or statistical test where methods are compared.
- **Use two or three significant digits** unless more precision is meaningful. "90.5934 ± 1.1426" implies a precision the data do not have.
- **Report ablations and null results directly**, for example: "Removing the auxiliary loss changed test accuracy by less than one standard deviation."
- **Do not invent numbers.** If a value is missing, flag it.

| Do | Avoid |
|---|---|
| The proposed model reached an MAE of 3.4 ± 0.2 objects per image (10 × 10-fold CV), compared with 4.1 ± 0.3 for the strongest baseline (Table 4). | As can be seen, the proposed method clearly and significantly outperforms all other methods. |

## 23. Discussion

**Purpose:** to interpret the results, connect them to prior work and set their limits.

1. **Answer the research question in the first sentence**, with the key number.
2. **Interpret the main findings.** Explain why they occurred, and separate explanations you tested from those you did not.
3. **Compare with prior work.** Include results that are worse than earlier studies, including your own earlier versions, and list the concrete differences that could explain the gap.
4. **Limitations.** One paragraph or a short list (see [§24](#24-limitations)).
5. **Future work.** Two or three concrete next steps tied to the limitations, not a wish list.

Do not introduce new experiments or numbers that are absent from Results. Do not add background that belongs in the Introduction, and do not close with a general statement about the importance of the field.

## 24. Limitations

- Place limitations in the **Discussion**, as an enumerated paragraph ("First, … Second, … Finally, …") or a short list.
- For each limitation, state **what** it is, **what it could affect** and, where possible, **how it could be addressed**.
- Check these typical categories:
  - data size and diversity (sites, seasons, devices, populations);
  - label quality and how labels were obtained;
  - a time gap between measurement and ground truth;
  - statistical independence of samples (subimages from one source image, segments from one subject);
  - controlled versus real-world acquisition conditions;
  - hyperparameters tuned on the data used for evaluation;
  - timing claims based on a single hardware and software configuration.
- **Do not bury limitations** in the Conclusion, and do not reframe them as strengths.
- Elsewhere in the paper, place a limitation next to the claim it restricts. Avoid opening every statement with a defensive disclaimer.

> **Do:** "Third, the image patches are not statistically independent: up to 50 patches come from one specimen. Aggregating results per specimen (Table 6) partly addresses this, but with nine specimens the per-specimen estimates remain uncertain."
>
> **Avoid:** "The study has some limitations which should be addressed in future work."

## 25. Conclusion

- One paragraph or three to six bullets, readable without the rest of the paper.
- Restate **what was done, the main quantitative result and its scope**.
- Answer the aims stated in the Introduction if the Discussion has not already done so.
- **Introduce nothing new**: no new citations, mechanisms or background. A Conclusion that opens with new domain theory is misplaced Discussion.
- If the venue merges the Discussion and Conclusion, follow [§23](#23-discussion) and end with the scoped take-away.

## 26. Software and tool papers

- Explain the **design rationale** for the dependencies, the shape of the API and the class hierarchy.
- Show **minimal working code** for each feature. It must run exactly as printed. Copy it from the repository rather than retyping it.
- Compare with existing packages in a **table of features, dependencies and licences**, without claiming superiority.
- Describe **testing, documentation and release practice** in its own paragraph.
- Support statements about adoption with evidence such as download counts or issue statistics, not impressions.
- Check every displayed update rule against the code (see the [notation guide](mathematical_notation_guidelines.md#3-apply-the-notation-throughout-the-article)).

## 27. Figures, tables, numbers and citations

### 27.1 Figures and tables

- Refer to every figure and table in the text, in the order in which they appear.
- **Every caption must be understandable without the main text.** It defines its abbreviations, states units, says what bold or ± means, and tells the reader what to look at, not only what is plotted.
- Table headers carry units. Use the same number of decimal places within a column.
- Legends and annotations must not hide data. Place them outside the plotting area when practical.
- Check figures at their final typeset size: all labels must fit inside their regions and remain legible.

### 27.2 Numbers

- Give every number with its unit.
- Use the same number of decimal places for the same kind of quantity throughout the paper.
- Report uncertainty (standard deviation or confidence interval) with every estimate, and state which one it is.
- Keep numerical values, units, conditions and uncertainty intact when editing.

### 27.3 Citations

- Attach each citation to the specific claim it supports.
- A citation does not replace explaining the method.
- Never invent references, author names, results or citation numbers.

## 28. Pre-submission checklist

**Content and structure**

- [ ] The abstract follows the order in §17, contains the main quantitative result and the validation scheme, and has no citations or figure references.
- [ ] The Introduction ends with the aim and a contribution list, and every item can be checked.
- [ ] Related Work is grouped by approach, contains no details of the present study, and ends with the positioning.
- [ ] Every design choice and hyperparameter has a stated reason.
- [ ] The unit the data were split by and the leakage control are stated.
- [ ] Every result has a spread and a run count. Comparative claims name a baseline and a metric, and include an effect size or a test where appropriate.
- [ ] Null and negative results are reported plainly.
- [ ] The Discussion opens with the answer, includes a limitations paragraph and gives concrete future work.
- [ ] Every aim from the Introduction is answered.
- [ ] The Conclusion introduces nothing new.

**Language** (see Part I)

- [ ] "We" is used consistently. No term varies for the same concept.
- [ ] Abbreviations are defined at first use in the abstract and again in the main text. None appear in the title or headings.
- [ ] Hedging matches the evidence. "Significant" is used only for statistical significance.
- [ ] The text has been searched for the phrases in [§11](#11-generic-ai-sounding-expressions) and [§12](#12-unnecessary-jargon-and-wordiness).
- [ ] The text has been checked for the errors in [§14](#14-common-language-errors): articles, spelling in headings and captions, duplicates and leftover draft notes.
- [ ] No sentence would fit unchanged into a paper on another topic. The text reads like a careful researcher, not a language model imitating academic prose.

**Integrity**

- [ ] No facts, numbers, parameters or citations were invented, and every original value, unit, condition and citation survived editing.
- [ ] Missing information is flagged for the authors, not filled in.

**Mathematics, figures and availability**

- [ ] The [notation audit](mathematical_notation_guidelines.md#4-validate-after-drafting-and-after-every-mathematical-revision) passes.
- [ ] Every figure and table is referenced in order, its caption stands alone, and it is legible at print size.
- [ ] The data and code availability statements are complete, and their links work.
