---
title: "01 Introduction 导论"
format: 
  html:
    code-fold: false
    code-tools: true
editor: visual
---





::: callout-tip
## Page with R code

This page contains an example template for a lab session, where **R code
and results** are displayed here.

You can find more information on how to include code in Quarto website
[here](https://quarto.org/docs/reference/cells/cells-knitr.html).

You can experiment with `code-fold` and `code-tools` in the yaml header
above to change how the code cells look like.
:::

## A Cancer Modeling Example

Exercise on analysis of miRNA, mRNA and protein data from the paper Aure
et al, Integrated analysis reveals microRNA networks coordinately
expressed with key proteins in breast cancer, Genome Medicine, 2015.

Please run the code provided to replicate some of the analyses. Make
sure you can explain what all the analysis steps do and that you
understand all the results.

In addition, there are some extra tasks (`Task 1`), where no R code is
provided. Please do these tasks when you have time available at the end
of the lab.

### Load the data

Read the data, and convert to matrix format.




::: {.cell}

```{.r .cell-code}
mrna <- read.table("data/data_example.txt", header=T, sep="\t", dec=".")

# Convert to matrix format

mrna <- as.matrix(mrna)
```
:::




Print the data




::: {.cell}

```{.r .cell-code}
mrna[1:4, 1:4]
```

::: {.cell-output .cell-output-stdout}

```
      OSL2R.3002T4 OSL2R.3005T1 OSL2R.3013T1 OSL2R.3030T2
ACACA      1.60034     -0.49087     -0.26553     -0.27857
ANXA1     -2.42501     -0.05416     -0.46478     -2.18393
AR         0.39615     -0.43348     -0.10232      0.58299
BAK1       0.78627      0.39897      0.22598     -1.31202
```


:::
:::




Visualise the overall distribution of expression levels by histogram




::: {.cell}
::: {.cell-output-display}
![](part_2_eda_files/figure-beamer/unnamed-chunk-3-1.pdf)
:::
:::




::: callout-note
## Task 1

*This is a callout-note, and it can be quite useful for exercises. You
can find more about callout
[here](https://quarto.org/docs/authoring/callouts.html).*

Example: Extend the above analysis to cover all genes.
:::
