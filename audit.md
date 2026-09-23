# Audit

Dated log of editorial passes and verification runs. Newest first.

## 2026-09-23 — structured-evidence migration

Structured-evidence migration (references and claims).
- references.yaml: 47 CSL entries. 14 matched automatically in Crossref and resolved through doi.org; hoel2017, hollan2000, sterelny2010, watson2016, henrich2016, lave1991, malafouris2013, netz1999 and varela1991 matched by hand to DOI records (subtitles restored); pigozzi2026 entered from its arXiv record (2605.06746). 22 books entered by hand from the legacy text with publisher places (existence confirmed through OpenAlex book or review records); levin2025b entered as a lecture with its URL. In-text author-year citations converted to Pandoc [@id] syntax; the legacy reference list replaced by the citeproc-rendered list (Chicago author-date).
- No bibliographic or numerical corrections. varela1991 keeps the title-page author order (Varela, Thompson, Rosch) against the MIT Press record's order. Citeproc assigns the 2025 Levin suffixes by title, so levin2025b (lecture) renders as 2025a and levin2025a (PsyArXiv) as 2025b; the citations point to the same works as before.
- claims.yaml: 30 claims (15 source, 4 definition, 3 assumption, 7 interpretation, 1 normative). Source claims checked against Crossref or OpenAlex abstracts, the arXiv abstract of Pigozzi and Levin 2026, and the open-access text of Pigozzi et al. 2025 (which names the "intelligence ratchet").
- Not bound (no retrievable abstract or support beyond the record): the Latour, Knorr Cetina, Galison, Daston and Galison, Shapin, Danziger, Carson and Gould readings; Clark and Chalmers on Otto's notebook; Adams and Aizawa and Rupert's critique; Sterelny on scaffolding; Rotman; Levin's ingression framing (levin2025a, no abstract) and the lecture slide (levin2025b); Watson and Szathmáry (no abstract).
- Flag for the author: the sentence citing Gould 1981 and Carson 2007 for the claim that measured differences "predict outcomes" cites two critics of intelligence testing for a claim they discuss rather than establish; left unchanged.
- metadata claims_target: claim-ledger.

## 2026-09-23 — prose revision

Headings now: Abstract; 1. Introduction; 2. Latour's Modern Constitution; 3. The Cognitive Constitution; 4. Capacity, Performance, Realization, and Historical Possibility; 5. Extension, Scaffolding, and Attributional Compression; 6. Six Cases of Attributional Compression; 7. Attribution as an Accounting System; 8. The Biological Floor and the Free-Lunch Hypothesis; 9. Scope and Limits; 10. Conclusion (split from the closing paragraphs of the former Section 9).
Tic counts before -> after (diag.py): rather than 10 -> 0; inline ", not X" 4 -> 0; negate-pivot 7 -> 0; "not X but Y" 14 -> 0; "the paper/this paper" 13 -> 0; exactly/precisely 5 -> 0; merely/simply 2 -> 0; worth 4 -> 1 ("a data centre's worth of compute", literal).
Abstract rewritten to 259 words without self-reference or rhetorical opener.
Corrections: Section 8 referred three times to "the next section" as the place that leans on the biological floor and warns against intelligence-mysticism; those passages are in Sections 4 and 9, and the cross-references now name them. Table 1 is now introduced in the text.
Numbers: conceptual paper with no simulation; the only numerals are years and bibliographic locators, all preserved. No grid audit applicable.

## 2026-06-20 — Added the math-not-biology turn (Levin/Pigozzi)
Scope: deepening pass prompted by Michael Levin's lecture "Free Lunches: Model Systems for Studying the Agential Gifts from the Platonic Space" and the Pigozzi-credited slide "The intelligence ratchet is a gift from Math, not from Physics or Biology."
Decision: integrate as a new movement rather than a bolt-on. The thesis extends the paper's master move (relocate the credit one level further out, past biology itself) while also pressuring it (the paper is deflationary/Latourian; Levin is realist/Platonist). Staged the encounter and reused the paper's own §5 move: decline the Platonic metaphysics, keep the deflationary phenomenon.
Changes:
  - New §8 "The Gift Nobody Made": the regress does not stop at the species. If learning is a generic affordance of mathematical structure that selection discovers rather than builds (random unselected networks already near-optimal), then crediting human biology for intelligence is attributional compression at the largest scale, an author at no level. Objection folded in (cuts against the §9 biological floor), answered two ways (levels-do-not-collide; the claim was always about who gets billed, not the ultimate source). Closing caution against re-enchantment ("a gift from math" can become intelligence-mysticism in a Platonist's robe).
  - Renumbered old §8 -> §9; revised its "does not deny biology" paragraph so enrollability reads as the quality of one interface onto an older, generic capacity rather than the capacity's origin, removing the flat contradiction with §8.
  - Abstract (paper + metadata + web entry) extended with one sentence on the deepest relocation.
  - Bibliography grew 36 -> 47. Added, all engaged in-text and verified: Levin 2022 (TAME, Front. Syst. Neurosci.); Levin 2025a (Ingressing Minds, PsyArXiv preprint, flagged as not-yet-peer-reviewed); Levin 2025b (the lecture, cited as a talk, Pigozzi slide credited on-screen); Pigozzi, Goldstein & Levin 2025 (Comms Biology, the published home of the "intelligence ratchet" phrase); Pigozzi & Levin 2026 (arXiv); Hoel/Albantakis/Tononi 2013 and Hoel 2017 (causal emergence); Klein & Hoel 2020 (causal emergence in networks); Watson & Szathmary 2016 and Vanchurin/Wolf/Katsnelson/Koonin 2022 (learning as generic to dynamical matter); Walker & Davies 2013 (causal structure prior to replicators).
  - Honesty discipline: the strongest slide claims (random-network optimality; "math not biology") are marked talk-stage/in-progress in the prose; the Platonic metaphysics is named contested and probably unfalsifiable and explicitly declined. Corrected the common mis-citations flagged in research (Yuri I. Wolf, not Wolpert; Walker & Davies 2013, not 2012; Klein & Hoel 2020 is the Complexity paper, not the einet repo).
Verification:
  - voice: 0 errors, 14 review-candidate warns (negate-pivot / inline-contrastive, intrinsic to the argument). Reworded two pet-vocabulary phrases I introduced ("the whole story", "earns its keep").
  - refs: 0 missing, 0 unused (47 bib entries).
  - claims: none (no simulation).
  - build: clean, 0 missing-character warnings. PDF synced to web.
  - check => PASS

## 2026-06-19 — Initial implementation from seed chat
Scope: full paper built from `chats/chat.md` (a deep-research dump on the Latour-inspired thesis) through the PIATRA pipeline.
Decision: built deliberately as a no-simulation genealogy/synthesis, to break the corpus's recurring parametric-model-plus-threshold template. A scaffold-ablation model (the seed's §7.7) was declined because it would rhyme with the existing credit-assignment paper and with the threshold fingerprint.
Changes:
  - Took the seed's central contribution (the Cognitive Constitution and "attributional compression") and sharpened it with a political edge: purification is the accounting system of merit, which is why the individual mind survives every demonstration of its insufficiency. Intelligence names a settlement about credit, not a measurement of where thinking happens.
  - Honored the user's unqualified title `We Have Never Been Intelligent` while using the destabilize-then-qualify move the seed recommended (the defensible thesis is "never intelligent alone").
  - Spine: the capacity / performance / realization / historical-possibility distinction, used to defuse the false psychometrics-vs-distributed-cognition rivalry. Claim-strength discipline: rests on the dependency and explanatory-unit claims, declines the contested metaphysical "constitution" claim (Adams-Aizawa, Rupert, Sterelny granted).
  - Structure breaks the schematic skeleton: distinctive section titles, objections folded into a closing "What the Argument Leaves Standing," no ceremonial conclusion; ends on the political residue rather than a "does X not Y" formula.
  - 36-source bibliography, all engaged in-text, verified against the real literature; Hayles (2017) acknowledged for prior "cognitive assemblage" usage; 0 confabulated (refs MISSING = 0).
  - Wrote metadata.yaml (title, abstract, has_simulation false, claims_target none), brief/research/sources, README.
Verification:
  - voice: 0 errors, 16 review-candidate warns (negate-pivot / inline-contrastive, intrinsic to a not-X-but-Y argument). Purged the `load-bearing` pet-word (incl. a section title); thinned `exactly`/`carry`.
  - refs: 0 missing, 0 unused (36 in-text keys, 36 bib entries).
  - claims: none (no simulation; manual claims only).
  - build: 11 pages, 0 missing-character warnings.
  - check => PASS
