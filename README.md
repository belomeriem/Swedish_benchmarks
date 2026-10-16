 # Swedish LLM Benchmark Overview
This is the repository for summarising existing Swedish Benchmarks. These are resources for a Swedish LLM leaderboard, grouped by track and area.

**Contents**

- [Open design question](#open-design-question)
- [Track A: Swedish linguistic competence](#track-a-swedish-linguistic-competence)
- [Track B: General capabilities in Swedish](#track-b-general-capabilities-in-swedish)
- [Translation](#translation)
- [Local and cultural knowledge](#local-and-cultural-knowledge)
- [Instruction following](#instruction-following)
- [Domain-specific knowledge](#domain-specific-knowledge)
- [Alignment with legal norms](#alignment-with-legal-norms)
- [Track C: Communicative competence](#track-c-communicative-competence)
- [Notes](#notes)

## Open design question

Should this leaderboard evaluate only Swedish-language competence and quality, or should it also be a general LLM leaderboard conducted entirely in Swedish, comparable in scope to the [Open LLM Leaderboard](https://huggingface.co/open-llm-leaderboard)?

## Track A: Swedish linguistic competence

Language-specific. Covers syntax, morphology, lexical semantics, acceptability, discourse and pragmatics.

### Acceptability, syntax and morphology

| Benchmark / resource | What it evaluates | Status | Relevance, priority and notes | Source |
|---|---|---|---|---|
| Swedish BLiMP (Swedish Benchmark of Linguistic Minimal Pairs, 2026) | Syntax and grammaticality, 25 syntactic phenomena | Existing | Core for grammaticality | [LREC 2026](https://aclanthology.org/2026.lrec-1.540.pdf) |
| Swedish MultiBLiMP | Grammatical minimal pairs | Existing | Considered trivial. Extensions are ongoing (Joakim is involved) | [TACL 2026](https://aclanthology.org/2026.tacl-1.10.pdf) |
| UniMorph-BLiMP (Swedish) | Morphology, BLiMP-style | Existing, with a human-verified subset | Complements Swedish BLiMP | [Dataset](https://huggingface.co/datasets/liu-nlp/unimorph-blimp-growup/viewer/swe), [verified subset](https://huggingface.co/datasets/anjajar/swedish_samples_v2) |
| DaLAJ 1.0 | Binary acceptability judgments on 9,596 sentences, mainly lexical and word-formation errors | Existing | Very high for acceptability. Top-5 priority. Jenny has a minimal-pairs version | [Volodina et al. 2021](https://aclanthology.org/2021.nlp4call-1.3.pdf) |
| DaLAJ-GED (SuperLim 2.0) | Grammatical error detection | Existing | Top priority. Learner errors do not cover every type of LLM error. Its original use case (error correction) complements Swedish BLiMP | Volodina et al. 2023 |
| ScaLA | Scandinavian linguistic acceptability | Existing | Very high for grammaticality. With DaLAJ, the strongest starting point for acceptability | n/a |
| SweLL | Learner language, error correction, word choice, morphology | Existing | High for error analysis and controlled tests. Top-5 priority | n/a |
| Svensk trädbank / Talbanken | Syntax, morphology, dependency structures | Existing | High for structural correctness | n/a |
| Translationese and idioms (Jenny) | Translationese, idiomaticity | Partly closed (usable internally) | Links to the Track C idiomaticity focus | [TACL 2026](https://aclanthology.org/2026.tacl-1.57.pdf), [LREC 2026](https://aclanthology.org/2026.lrec-1.690.pdf) |

## Track B: General capabilities in Swedish

Leaderboard-compatible. Covers reasoning, knowledge, instruction following, factuality and reading comprehension.

| Benchmark / resource | What it evaluates | Status | Relevance, priority and notes | Source |
|---|---|---|---|---|
| SuperLim 2.0 (SweBench) | Broad Swedish language understanding (GLUE-like) | Existing | Use relevant subtasks, not the overall score, as a fluency measure | [AI Sweden](https://www.ai.se/en/project/superlim), Berdicevskis et al., EMNLP 2023 |
| EuroEval (Swedish) | Many tasks | Mostly 5-shot | For instruction-tuned models, also run 0-shot | [EuroEval](https://euroeval.com/datasets/swedish) |
| Open LLM Leaderboard tasks | Many LLM test cases | Translate to Swedish or select applicable ones | Depends on the design question above | [Leaderboard](https://huggingface.co/open-llm-leaderboard) |
| Global MMLU (Swedish MMLU) | Knowledge and reasoning | Existing | | [ACL 2025](https://aclanthology.org/2025.acl-long.919.pdf) |
| MGSM | Math reasoning | To check | | n/a |
| Global PiQA | Physical commonsense | Existing | | [arXiv 2510.24081](https://arxiv.org/pdf/2510.24081) |
| TruthfulQA | Factuality | Listed in Track B | Status not specified | n/a |
| Reading comprehension | Reading comprehension | Listed in Track B | Status not specified | n/a |
| SweSAT | Reading comprehension, language proficiency | Partly in EuroEval's Skolprov (5-shot), extent unclear | Useful for advanced linguistic understanding | [NoDaLiDa 2025](https://aclanthology.org/2025.nodalida-1.36.pdf) |
| SweFAQ 2.0 | Question answering | Existing | Useful for semantic adequacy, not direct fluency | n/a |
| Swedish portions of multilingual suites | General language modeling, instruction following | Existing | Complementary evaluations | n/a |

## Translation

| Benchmark | Status | Notes | Source |
|---|---|---|---|
| WMT24++ | In EuroEval (5-shot) | | n/a |
| FLORES+ | In EuroEval (5-shot) | | n/a |
| BOUQUET | To check | | n/a |
| The Last Translation Benchmark | Only 2 Swedish examples so far | Worth watching, as it is continuously developed | [arXiv 2609.04173](https://arxiv.org/pdf/2609.04173) |

## Local and cultural knowledge

| Benchmark / resource | Status | Notes | Source |
|---|---|---|---|
| MultiLoKo | Covers Swedish, not yet reviewed | | [arXiv 2504.10356](https://arxiv.org/pdf/2504.10356) |
| MRL shared task 2026 | Unclear whether Swedish is covered | Find out who is involved | [MRL benchmarks](https://mrlbenchmarks.github.io/) |
| Jenny's factual QA dataset | In EuroEval as multiple-choice with LLM-generated alternatives (5-shot) | | [LREC 2026](https://aclanthology.org/2026.lrec-1.416.pdf) |
| Cultural Grounding in Swedish (Meriem) | Extension of an everyday-knowledge benchmark | | n/a |

## Instruction following

| Benchmark | Status | Notes | Source |
|---|---|---|---|
| MAXIFE | Includes Swedish | Quality needs checking | [ACL 2025](https://aclanthology.org/2025.acl-long.698.pdf) |
| MultiIFEval | In EuroEval (0-shot) | | [EuroEval](https://euroeval.com/datasets/swedish) |
| IFEval | Listed in Track B | Status not specified | n/a |

## Domain-specific knowledge

| Benchmark / resource | What it evaluates | Status | Source |
|---|---|---|---|
| Journalism benchmark (Lukas) | Headline and lead generation, bullet-point summaries, topic classification, salient NER, multiple-choice quizzes | Not open, usable internally | [arXiv 2608.30609](https://arxiv.org/pdf/2608.30609) |
| SVD SEO Title | Headline generation | Unofficially in EuroEval (1-shot) | [Hugging Face](https://huggingface.co/datasets/Schibsted/svd-seo-title) |
| Swedish medical benchmark | Medical knowledge | Existing | [GitHub](https://github.com/BirgerMoell/swedish-medical-benchmark/) |
| MedQA-SWE | Medical QA | Existing | [LREC-COLING 2024](https://aclanthology.org/2024.lrec-main.975.pdf) |
| Multilingual Healthcare Benchmarking for Swedish | Healthcare | Just started as a NAISS project, worth contacting | [SUPR project 39033](https://supr.naiss.se/public/project/39033/) |

## Alignment with legal norms

| Resource | Status | Source |
|---|---|---|
| Legal-norms alignment paper | Translate to Swedish and/or use in English | [arXiv 2510.21524](https://arxiv.org/pdf/2510.21524) |


