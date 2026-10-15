---
title: "Chapter 2: Random Variables and Probabilities"
course: Design of Experiments
date: 2026-10-15
tags: [probability, random-variables, normal-distribution, lognormal-distribution, pdf, cdf]
source: incoming/Chapter 2_ Random Variables And Probabilities.pdf
status: final
---

## Random variables

Random variables can be discrete or continuous.

## Probability

Probability: degree of belief or relative frequency.

- $P(A)$: probability of event $A$
- Not $A$ $\rightarrow$ $P(A')$
- "and": $P(A \cap B)$, joint probability
- "or": $P(A \cup B)$, union probability
- $P(A \mid B)$: conditional probability

Mutually exclusive / disjoint:

$$
P(A \cap B) = 0
$$

Independent:

$$
P(A \cap B) = P(A)\,P(B)
$$

## Rules

$$
P(A) \in [0, 1]
$$

$$
P(A') = 1 - P(A)
$$

$$
P(A \cup B) = P(A) + P(B) - P(A \cap B)
$$

$$
P(A \cap B) = P(A \mid B)\,P(B) = P(B \mid A)\,P(A)
$$

$$
P(A \mid B) = \frac{P(A \cap B)}{P(B)}
$$

$$
P(A \cup B) \geq P(A)
\qquad
P(A \cap B) \leq P(A)
$$

## Visualizing probabilities

- PMF: probability mass function
- PDF: probability density function
- CDF: cumulative distribution function

Conversions between them:

- PDF $\xrightarrow{\text{integrate}}$ CDF, and CDF $\xrightarrow{\text{differentiate}}$ PDF
- PMF $\xrightarrow{\text{sum up}}$ CDF
- PMF $\xrightarrow{\text{fit}}$ PDF, and PDF $\xrightarrow{\text{bin}}$ PMF

## Normal distribution

- $\mu$: mean
- $\sigma$: standard distribution

PDF:

$$
f(x) = \frac{1}{\sigma\sqrt{2\pi}} \, e^{-\frac{1}{2}\left(\frac{x - \mu}{\sigma}\right)^2}
$$

CDF:

$$
F(x) = \frac{1}{2}\left[1 + \operatorname{erf}\left(\frac{x - \mu}{\sigma\sqrt{2}}\right)\right]
$$

## Lognormal distribution

$$
X = \ln(Y)
\qquad
Y = e^{\mu + \sigma X}
$$

Note: $\mu, \sigma$ are just symbols, not the mean and standard deviation.

Mean:

$$
\exp\left(\mu + \frac{\sigma^2}{2}\right)
$$

Variance:

$$
\left[\exp(\sigma^2) - 1\right] \exp(2\mu + \sigma^2)
$$

PDF:

$$
f(x) = \frac{1}{x\sigma\sqrt{2\pi}} \exp\left(-\frac{(\ln(x) - \mu)^2}{2\sigma^2}\right)
$$

CDF:

$$
F(x) = \frac{1}{2}\left[1 + \operatorname{erf}\left(\frac{\ln(x) - \mu}{\sigma\sqrt{2}}\right)\right]
$$
