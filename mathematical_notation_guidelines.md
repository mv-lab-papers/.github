# Mathematical formalism and notation

Apply these instructions when drafting, revising, or reviewing any mathematical content in a manuscript. Cover the entire article, including the abstract, inline mathematics, displayed equations, algorithms, figures, tables, captions, appendices, and supplementary material.

This guide is part of the [publication guidelines](README.md). For general style and paper structure, see [writing_guidelines.md](writing_guidelines.md).

**In short:** introduce each equation with a sentence that says what it computes. Follow it with a `where …` clause that defines every new symbol, its domain and its units. Number every displayed equation. Use one symbol per concept everywhere. Check equations against the code. Keep only the equations that do identifiable work in the paper.

## 1. Design notation before editing equations

1. Inventory the equations and identify the quantities, mathematical objects, indices, operators, and assumptions they require. Read the whole manuscript before choosing notation for an individual section.
   For each equation, also record its purpose, inputs, output, and the specific downstream step that uses it (a derivation, algorithm, simulation event, evaluation, or interpretation of a result). Decide whether to retain, integrate, or remove it before polishing its notation.
2. Create a working notation register with these columns: concept, canonical symbol (including indices and typographic style), meaning, mathematical type and domain, units or dimensions where applicable, index ranges, and location of first use and definition. Record conventions for families of symbols rather than listing every indexed instance separately.
3. Choose one canonical notation for each concept across the article. Reserve each symbol for one meaning; do not reuse it for an unrelated quantity in another section or appendix. Use explicit, consistently defined indices or qualifiers for related quantities.
4. Follow established notation in the relevant discipline when it is applicable. Check authoritative references already used by the manuscript or relevant primary literature when a convention is uncertain. Do not invent a convention or claim that a personal preference is standard. Where disciplines conflict, select and document one coherent convention suited to the article's audience.
5. Resolve collisions before rewriting. When adapting a formula from a source, translate its notation into the article's notation and explain the mapping where readers need it. Record any necessary departure from a standard convention and explain it at first use.

Keep the register as a working review artifact; a published notation table is optional and does not replace definitions in the text. Do not add unused symbols merely to complete a notation system.

## 2. Define every symbol at its first use

- Introduce each displayed equation with a sentence that says **what it computes or asserts**. Put the definitions in a `where …` clause directly after the equation.
- State **domains and dimensions** explicitly, e.g. \(e(k) \in \mathbb{R}\), \(\mathbf{w}(k) \in \mathbb{R}^{n}\), \(k \in \mathbb{Z}\).

| Do | Avoid |
|---|---|
| The prediction error is \(e(k) = d(k) - \hat{y}(k)\), where \(d(k) \in \mathbb{R}\) is the target and \(\hat{y}(k) \in \mathbb{R}\) is the filter output at discrete time index \(k\). | The error is computed as usual. |

- Introduce each manuscript-specific symbol before its first occurrence or in prose immediately following the first equation in which it occurs. A reader must be able to understand that first equation without searching later sections or a notation table. If a symbol appears earlier in inline mathematics, define it there.
- Explain every newly introduced element of that equation: quantities, parameters, constants, sets, functions, random variables, indices, index ranges, subscripts, superscripts, and nonstandard operators. Give the meaning, type or domain, and units where applicable. Explain what indices and qualifiers represent; a variable name alone is not a definition.
- Standard arithmetic and universally understood mathematical syntax need no glossary entry. State the interpretation of any notation whose meaning depends on the field or context, including norms, expectations, probabilities, transforms, and overloaded operators.
- Distinguish objects that have different mathematical roles: a random variable and its realization, a population quantity and its estimate, a function and its value, a scalar and a vector or matrix, and continuous time and a discrete index. Define typography, hats, bars, and other modifiers consistently.
- Define assumptions and validity conditions before or alongside the equation that needs them, including distributional assumptions, independence, admissible parameter values, and boundary or initial conditions where relevant.
- Treat the abstract and main text as independently readable: define symbols again at first use in the main text, keeping the same meaning and notation. Define notation needed to read standalone captions or supplementary documents locally as well, without introducing alternative meanings.

For example, the first occurrence of

\[
\bar{t} = \frac{1}{n}\sum_{i=1}^{n} t_i
\]

must explain that \(n \geq 1\) is the number of observations, \(i \in \{1,\ldots,n\}\) indexes them, \(t_i\) is the duration of observation \(i\) in seconds, and \(\bar{t}\) is their arithmetic mean in seconds. This example illustrates definition placement; choose actual symbols according to the manuscript's field and notation register.

## 3. Apply the notation throughout the article

- Use the canonical symbol and meaning everywhere, including prose references, plots, tables, pseudocode, and appendices. Do not switch letters, capitalization, font style, index order, or modifiers for the same object.
- Use consistent conventions for scalars, vectors, matrices, sets, functions, operators, units, and descriptive subscripts. Follow the journal's typography requirements where specified.
- Keep equations mathematically compatible: domains, dimensions, units, index bounds, conditioning, and assumptions must agree. State any conversion, normalization, approximation, or change of variables explicitly.
- Preserve the mathematical meaning when renaming symbols. Apply changes to all occurrences and their definitions; check for collisions with symbols already present. Do not perform an unchecked global text replacement.
- Explain what each important equation computes or asserts and how it contributes to the argument. State whether a relation is a definition, an identity, an assumption, an approximation, or an empirical model when this is not evident.
- Number all displayed equations and refer to them by number. Do not write "the formula above" or "the following equation".
- Derive or state an equation once. Later sections refer back to it by number instead of repeating it, unless repetition is genuinely needed for readability.
- When the paper describes implemented code (an update rule, a loss, a metric), **check every displayed formula against the implementation**. In software papers, render the equation and the printed code snippet from the same source. Typesetting errors such as a missing factor or a wrong variable in an update rule easily survive review.

### Require a functional role for every equation

Correct notation and complete definitions are necessary but insufficient. Every displayed equation must do identifiable work in the article. For each one, answer: **What later calculation, procedure, inference, or interpretation depends on this equation, and where is that dependency explained?** A nearby paraphrase, a repeated symbol, an equation-number reference, or a statement that the quantity is important does not establish that dependency.

Choose one of two outcomes:

1. **Remove unnecessary formalism.** If a definition or list of measured quantities can be stated clearly in prose or a table and no subsequent reasoning needs its symbolic form, replace the displayed equation with that explanation. Remove unused symbols and update references and the notation register. Merely moving an unused formula into inline mathematics or an appendix does not solve the problem.
2. **Integrate necessary formalism.** If the equation is needed to explain the method or result, show how its inputs are obtained, how its output is used, and how it connects to the subsequent reasoning. Supply the missing derivation, algorithm, event rules, or evaluation step, at the level needed to reconstruct the method. Use equations, pseudocode, or precise prose as appropriate; do not add equations solely to create apparent reuse.

A definition can legitimately be a terminal quantity, such as an evaluated metric or a reported theoretical result. It need not feed another equation, but the article must explicitly connect it to the actual evaluation, reported result, or scientific interpretation. Repetition for its own sake is not a requirement.

For a simulation model, explain the complete relevant path from measured inputs to predicted outputs: how observations are sampled or combined, what state and events the simulator maintains, how events update that state, how conflicts or simultaneous events are resolved when they affect the output, and how simulated outputs enter the reported evaluation. Define initialization and termination where they affect the result. If multiple model variants are compared, identify exactly which sampling rules, dependencies, or state transitions differ and which remain shared. A vector of component durations and a definition of output age do not, by themselves, explain an event simulator.

For example, retaining a service-duration vector requires explaining how each compared model samples or constructs it and how it determines worker completion. Retaining an age definition requires connecting simulated frame selection and completion timestamps to age samples and then to the evaluated distributions. Alternatively, describe the measured stages and age boundary in prose if their symbolic form is unnecessary. Verify these connections against the actual implementation or documented method; flag missing details rather than inventing an algorithm.

## 4. Validate after drafting and after every mathematical revision

Audit the rendered manuscript in reading order, using the notation register as the reference. Source searches can help locate occurrences but do not replace checking rendered equations and figure labels.

- [ ] Every symbol is defined at its first use; every first equation explains all newly introduced notation locally.
- [ ] Every displayed equation is introduced by a sentence that says what it computes, is numbered, and is referenced by number.
- [ ] Equations that describe implemented code match the implementation, and printed code snippets run as shown.
- [ ] Every displayed equation has a recorded purpose and a specific, explained use in a derivation, procedure, evaluation, reported result, or interpretation; no equation passes solely because its notation is correct.
- [ ] Definitions and input vectors connect to the method that consumes them; terminal metrics connect to the actual reported evaluation or result.
- [ ] The relevant path from model inputs through computation or simulation to evaluated outputs is reconstructable, including the differences among compared variants.
- [ ] Unnecessary equations and their unused notation have been removed rather than relocated or given superficial references.
- [ ] Every concept has one canonical notation, and no symbol has conflicting meanings anywhere in the article.
- [ ] Each occurrence agrees with the register in meaning, type, domain, units, indices, and typographic style.
- [ ] Discipline-specific conventions are followed, and necessary deviations are explained.
- [ ] Equations have compatible dimensions, valid domains and index bounds, and explicit assumptions where needed.
- [ ] Random quantities, observations, estimates, and other distinct objects remain distinguishable.
- [ ] Definitions precede dependent definitions; no explanation depends on notation introduced only later.
- [ ] Renamings are propagated to text, equations, algorithms, figures, tables, captions, appendices, and supplementary material.
- [ ] Reordering or inserting equations has not moved a symbol ahead of its definition.

For each unresolved issue, report the location, symbol, conflicting or missing definition, and proposed correction. Do not invent a mathematical meaning to make the audit pass. Finalize the mathematical revision only after the checks pass or explicitly report the remaining issues to the author.
