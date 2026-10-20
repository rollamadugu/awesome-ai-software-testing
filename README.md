# Awesome AI Software Testing [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of tools, research, benchmarks, and communities at the intersection of **artificial intelligence and software testing** — AI/LLM test generation, test oracles, self-healing automation, mutation testing, and the trustworthiness of AI-produced verdicts.

AI now **writes** tests, **heals** them, and **judges** whether they pass. This list collects the best resources for building with that reality — and for staying skeptical about it. Curated by [Krishnasai Rollamadugu](https://github.com/rollamadugu), a test automation architect researching trust in AI-driven testing.

## Contents

- [Foundational reading](#foundational-reading)
- [AI & LLM test generation](#ai--llm-test-generation)
- [Test oracles & LLM-as-judge](#test-oracles--llm-as-judge)
- [Self-healing test automation](#self-healing-test-automation)
- [Mutation testing](#mutation-testing)
- [Flaky test detection](#flaky-test-detection)
- [Visual & AI-assisted UI testing](#visual--ai-assisted-ui-testing)
- [Benchmarks & datasets](#benchmarks--datasets)
- [Trustworthiness, calibration & evaluation](#trustworthiness-calibration--evaluation)
- [Communities & learning](#communities--learning)
- [Contributing](#contributing)
- [License](#license)

## Foundational reading

Start here to understand *why* AI in testing is hard, not just how.

- [The Oracle Problem in Software Testing: A Survey](http://www0.cs.ucl.ac.uk/staff/mharman/tse-oracle.pdf) — Barr, Harman, McMinn, Shahbaz & Yoo, IEEE TSE 41(5), 2015. The definitive survey of *how we decide a test passed* — the core problem AI oracles now inherit. [DOI](https://doi.org/10.1109/TSE.2014.2372785)
- [Software Testing with Large Language Models: Survey, Landscape, and Vision](https://arxiv.org/abs/2307.07221) — Wang et al., 2023/2024. Broad map of how LLMs are applied across testing tasks.
- [An Analysis and Survey of the Development of Mutation Testing](https://doi.org/10.1109/TSE.2010.62) — Jia & Harman, IEEE TSE, 2011. The reference survey on mutation testing, the basis for objective fault-detection measurement.

## AI & LLM test generation

Tools that generate test cases or whole suites automatically.

- [EvoSuite](https://github.com/EvoSuite/evosuite) — Search-based automatic test-suite generation for Java, optimising for coverage.
- [Pynguin](https://github.com/se2p/pynguin) — Automated unit test generation for Python.
- [Randoop](https://github.com/randoop/randoop) — Feedback-directed random test generation for Java.
- [Diffblue Cover](https://www.diffblue.com/) — Commercial AI unit-test writer for Java.
- [Qodo (formerly CodiumAI)](https://www.qodo.ai/) — AI test and code-integrity tooling integrated into the IDE.
- [Automated Unit Test Improvement using LLMs at Meta (TestGen-LLM)](https://arxiv.org/abs/2402.09171) — Alshahwan et al., 2024. LLM-generated tests gated by filters that require measurable improvement, reducing hallucinated tests.

## Test oracles & LLM-as-judge

The hardest part: deciding whether behaviour is *correct*, and using LLMs to do it.

- [Judging LLM-as-a-Judge with MT-Bench and Chatbot Arena](https://arxiv.org/abs/2306.05685) — Zheng et al., 2023. Foundational study of using strong LLMs as evaluators, and where they agree with humans.
- [Metamorphic testing](https://en.wikipedia.org/wiki/Metamorphic_testing) — A practical approach to the oracle problem using relations between inputs and outputs when a direct oracle is unavailable.

## Self-healing test automation

Frameworks that repair broken locators when the UI changes.

- [Healenium](https://healenium.io/) — Open-source self-healing extension for Selenium that recovers broken web locators.
- [Testim](https://www.testim.io/) — AI-assisted authoring with self-healing locators.
- [mabl](https://www.mabl.com/) — Low-code intelligent test automation with auto-healing.
- [testRigor](https://testrigor.com/) — Plain-English test authoring with resilient element matching.

## Mutation testing

Inject faults to measure whether tests actually *catch* bugs — objective ground truth for test strength.

- [PIT (pitest)](https://pitest.org/) — The standard mutation testing system for Java/JVM.
- [Stryker Mutator](https://stryker-mutator.io/) — Mutation testing for JavaScript/TypeScript, C#, and Scala.
- [mutmut](https://github.com/boxed/mutmut) — Mutation testing for Python.
- [MutPy](https://github.com/mutpy/mutpy) — Mutation testing tool for Python 3 with AST-level mutation.
- [Cosmic Ray](https://github.com/sixty-north/cosmic-ray) — Mutation testing for Python.
- [universalmutator](https://github.com/agroce/universalmutator) — Regexp-based mutation testing across many languages.

## Flaky test detection

Flakiness is where "trust the green" quietly breaks down.

- [DeFlaker](https://www.deflaker.org/) — Detects flaky tests from coverage of code changes without repeated reruns.
- [iDFlakies](https://github.com/idflakies/iDFlakies) — A framework to detect and classify order-dependent vs non-order-dependent flaky tests.

## Visual & AI-assisted UI testing

- [Applitools](https://applitools.com/) — Visual AI for UI validation and cross-environment comparison.
- [Percy (BrowserStack)](https://percy.io/) — Visual review and regression testing.

## Benchmarks & datasets

Shared ground truth for evaluating testing and program-repair techniques.

- [Defects4J](https://github.com/rjust/defects4j) — A database of reproducible real-world Java bugs, widely used in testing research.
- [BugsInPy](https://github.com/soarsmu/BugsInPy) — Real-world Python bugs for reproducible studies.
- [QuixBugs](https://github.com/jkoppel/QuixBugs) — Small multi-language buggy programs for repair/analysis.
- [SWE-bench](https://www.swebench.com/) — Benchmark of real GitHub issues for evaluating code-fixing agents.
- [HumanEval](https://github.com/openai/human-eval) — Hand-written programming problems for evaluating code-generation models.

## Trustworthiness, calibration & evaluation

Measuring *when an AI testing verdict can be believed* — the frontier this list is most interested in.

- [TrustLab](https://github.com/rollamadugu/trustlab) — Measures the "False-Confidence Gap" across AI oracles, self-healing, and LLM-as-judge, with a calibrated trust metric grounded in real mutation testing.
- [Expected Calibration Error (ECE)](https://en.wikipedia.org/wiki/Calibration_(statistics)) — Background on whether a model's confidence matches its real accuracy; essential for trusting AI verdicts.

## Communities & learning

- [Ministry of Testing](https://www.ministryoftesting.com/) — The largest software-testing community, forum, and conferences (TestBash).
- [Test Automation University](https://testautomationu.applitools.com/) — Free courses on automation and testing tooling.

## Contributing

Contributions are welcome. Please read [CONTRIBUTING.md](CONTRIBUTING.md). Entries must be **real, accurate, and relevant** — a working link, a one-line neutral description, and placement in the right section. Quality over quantity; no marketing fluff.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the curator has waived all copyright and related rights to this list (CC0 1.0). The linked resources remain under their own licenses.
