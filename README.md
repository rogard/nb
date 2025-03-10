# Jupyter notebooks

These jupyter notebooks are licensed as follows:

```plaintext
===============================================================================
 nb — notebooks
 Copyright (C) 2025 — Erwann Rogard
 Released under GPL 3.0
 See https://www.gnu.org/licenses/gpl-3.0.en.html
===============================================================================
```

## HHS false negative controversy

This relates to a [post on X](https://x.com/jeremykauffman/status/1898011686558196194) that states:  

> 4 out of 5 doctors at Harvard cannot answer a question from introductory statistics.  
>  
> *"If a test to detect a disease whose prevalence is 1/1000 has a false positive rate of 5%, what is the chance that a person found to have a positive result actually has the disease?"*

I claim one cannot solve the stated problem due to the unspecified false negative rate. I've provided a [Mathematica notebook](https://github.com/rogard/nb/blob/main/hhs-controv.ipynb) $\text{state}$ as "has the disease", $\text{outcome}$ as "result of the test", and $\text{ppv}$ as "chance that a person found to have a positive result actually has the disease".

$$
\text{ppv} = \frac{(1 - \text{falsenegrate}) \cdot \text{prevalence}}{\text{falseposrate} \cdot (1 - \text{prevalence}) + (1 - \text{falsenegrate}) \cdot \text{prevalence}}
$$

However, the derivative of $\text{ppv}$ in $\text{falsenegrate}$ (for short, $\text{p}$) is negative, such that the max is attained at $\text{p}=0$, which yields around $2%$.
