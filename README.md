# jamovi-modules-vm

A collection of [jamovi](https://www.jamovi.org) modules and related tooling, developed to customize or add functionality
Each module lives in its own repository; t See
each repo's own README for installation and usage details.

## Index
[https://victor-moreno.github.io/jamovi-modules-vm](https://victor-moreno.github.io/jamovi-modules-vm/)


## Which file do I download?

Each module's Releases page carries four `.jmo` files per version — one for each combination of
jamovi series and CPU:

| your jamovi | Apple silicon | Intel / AMD |
| --- | --- | --- |
| **current** (bundles R 4.6.0) | `<module>_<version>_current_R4.6.0_arm64.jmo` | `<module>_<version>_current_R4.6.0_x64.jmo` |
| **solid** (bundles R 4.5.0) | `<module>_<version>_solid_R4.5.0_arm64.jmo` | `<module>_<version>_solid_R4.5.0_x64.jmo` |

The same file works on macOS, Windows and Linux: jamovi's compatibility check covers the R version
and the CPU, not the operating system. Check **Help -> About** in jamovi if you are unsure which R
yours bundles. Then, in jamovi: **Modules -> jamovi library -> Sideload** and select the `.jmo`.


## Improvements to jmv

Modules that clone and extend jmv's built-in analyses.

- **[conttables2xK](https://github.com/victor-moreno/jamovi-conttables-2xK)** — extends jmv's
  Contingency Tables (Independent Samples) comparative measures (odds ratio, log odds ratio,
  relative risk, difference in proportions) from 2x2-only to 2xK tables.
- **[conttablespaired2xK](https://github.com/victor-moreno/jamovi-conttablespaired-2xK)** —
  extends jmv's Paired Samples Contingency Tables (McNemar) to non-binary paired responses (RxR
  tables), adding paired odds ratio, difference in proportions, marginal percentages and exact
  tests.
- **[corrInspect](https://github.com/victor-moreno/jamovi-corrInspect)** — redesign of jmv's
  Correlation Matrix with a tidy one-row-per-pair table, an inspector mode for one reference
  variable against several others, annotated scatterplots, and a colour-coded heatmap.
- **[regInspect](https://github.com/victor-moreno/jamovi-regInspect)** — clone of jmv's
  Linear Regression adding observed-data points (partial residuals by default) and prediction
  intervals to the Estimated Marginal Means plots, plus a descriptive Plots tab (scatter/box
  plots, colour-by-group, scatterplot matrix) independent of the model blocks.
- **[jmvplus](https://github.com/victor-moreno/jamovi-jmvplus)** — small additions to
  Descriptives (coefficient of variation) and Independent Samples T-Test (Fisher-Snedecor
  F-test alongside Levene's).
#### Install all together

- **[jamovi-combo](https://github.com/victor-moreno/jamovi-combo)** — bundles conttables2xK,
  conttablespaired2xK, corrInspect, regInspect and jmvplus into a single sideloadable `.jmo`, so
  installing all five is one "Sideload" instead of five. SNPstats, prognosis and jmsequential are
  released separately (see New additions below).


## New additions

New, domain-specific analyses.

- **[SNPstats](https://github.com/victor-moreno/SNPstats-jamovi)** — SNP analysis for genetic
  epidemiology: allele/genotype frequencies, Hardy-Weinberg equilibrium, SNP-response
  association, linkage disequilibrium, haplotype analysis and polygenic risk scores. Based on the
  [SNPstats web tool](https://www.snpstats.net). Since v1.1.0 it also **imports genotypes**
  from PLINK (`.bed`/`.bim`/`.fam`, `.ped`/`.map`, `.tped`/`.tfam`) and VCF files straight
  into a jamovi dataset — the former standalone
  [snpImport](https://github.com/victor-moreno/SNPstats-import) module, merged in as a third
  analysis after its jamovi review. Requires jamovi 28.4 or newer (since v1.2.1); on jamovi 28.3,
  use v1.2.0.
- **[prognosis](https://github.com/victor-moreno/jamovi-prognosis)** — Survival analysis for
  prognostic studies, with compact output aimed at teaching and reporting. Kaplan-Meier: median
  survival, survival at given times, log-rank and weighted rank tests (Gehan-Breslow, Tarone-Ware,
  Peto-Peto, trend) and survival plots with a number-at-risk table. Cox regression: univariable
  and multivariable hazard ratios, covariate HRs per unit, per SD or per a given value,
  interactions with subgroup HRs, proportional-hazards tests, forest plots and adjusted survival
  curves. Optional explanations for students; English, Spanish and Catalan. Comes with a
  tutorial for medical students (survival theory and worked examples in jamovi, on a teaching
  dataset).
- **[jmsequential](https://github.com/victor-moreno/jamovi-sequential)** — Sequential designs
  and monitoring for clinical trials, sequential experiments and safety surveillance, with
  control of the type I and type II errors. Group sequential designs: classical and
  error-spending boundaries, triangular tests, binding or non-binding futility; means,
  proportions and time-to-event endpoints (with accrual and dropout); interim monitoring with
  repeated confidence intervals, conditional power and adjusted final inference. Phase II
  multistage designs (Simon two-stage, Fleming, Bayesian) with exact operating characteristics.
  Wald's SPRT and sequential t-tests, MaxSPRT for post-marketing safety surveillance, Bayesian
  sequential monitoring, and anytime-valid e-values and confidence sequences. Comes with a
  [tutorial website](https://victor-moreno.github.io/jamovi-sequential/) on sequential methods,
  with each example worked in jamovi.

## Tooling

- **[jamovi-skill](https://github.com/victor-moreno/jamovi-skill)** — a Claude Code skill for
  building jamovi modules, distilled from developing SNPstats and snpImport plus a review of
  dev.jamovi.org and the jamovi source. Not a jamovi module itself.

## Deploying jamovi

- **[ondemand-jamovi](https://github.com/victor-moreno/ondemand-jamovi)** — an Open OnDemand
  interactive app that launches jamovi as a browser session on an HPC cluster.

## Upstream

- **[jamovi](https://github.com/jamovi/jamovi)** — the jamovi project itself.

<br />

## Acknowledments

This work has been developed with support of the Instituto de Salud Carlos III (ISCIII), “Programa FORTALECE del Ministerio de Ciencia e Innovación”, through the project number FORT23/00032 and the Consortium for Biomedical Research in Epidemiology and Public Health (CIBERESP), action Genrisk.

<br />

Claude Code was used to plan and implement in these projects.

<br />

## License

These projects are licensed under the **GNU General Public License v3**.

## Report issues

The code has not been extensively tested and could have bugs. Please use github Issues to report any problems and enhancement requests.

© Victor Moreno - [Catalan Institute of Oncology](http://iconcologia.net/)
