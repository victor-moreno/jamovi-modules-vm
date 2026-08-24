# jamovi-modules-vm

A collection of [jamovi](https://www.jamovi.org) modules and related tooling, developed to customize or add functionality

Each module lives in its own repository; this is an index page. See each repo's own README for installation and usage details.

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
- **[jmvplus](https://github.com/victor-moreno/jamovi-jmvplus)** — small additions to
  Descriptives (coefficient of variation), Scatter Plot (prediction interval), and Independent
  Samples T-Test (Fisher-Snedecor F-test alongside Levene's).

## New additions

New, domain-specific analyses.

- **[SNPstats](https://github.com/victor-moreno/SNPstats-jamovi)** — SNP analysis for genetic
  epidemiology: allele/genotype frequencies, Hardy-Weinberg equilibrium, SNP-response
  association, linkage disequilibrium, haplotype analysis and polygenic risk scores. Based on the
  [SNPstats web tool](https://www.snpstats.net).
- **[snpImport](https://github.com/victor-moreno/plink-importer)** — imports genotypes from
  PLINK (`.bed`/`.bim`/`.fam`, `.ped`/`.map`, `.tped`/`.tfam`) and VCF files into a jamovi
  dataset, ready for the SNPstats analyses. Developed standalone; being merged into SNPstats as a
  third analysis.

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
