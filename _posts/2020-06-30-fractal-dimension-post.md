---
layout: post
mathjax: true
title: A 0 dimensional uncountable set
categories: [blog, math]
tags: [blog, math]
---

# Intro

A while back I saw a post on Math StackExchange that asked why
any countable set has Hausdorff dimension 0 (, I'll comeback and add
a link to that post if I ever find it again). But it made me wonder if
that having non-zero dimension was a property that separated countable
sets from uncountable sets. I asked this question on Reddit, and 
by the time I woke up the next morning I had my answer: No.

So it turns out that we can construct an uncountable 0-dimensional set
in a process similar to getting a [fat cantor set][fat-cantor], but rather
than taking less and less from each interval in the construction, we actually
take more and more. Anyway, so I thought it would be cool to construct such
a set.

# Construction

To begin, we'll start with the set $ \Phi_0 = [0,1] $. Now, we're going
to remove the middle $ \frac{10^1 -1}{10^1} = \frac{9}{10}$ of $[0,1]$,
which then results in the two intervals $[0, \frac{1}{20}]$ and 
$[\frac{19}{20},1]$. Thus, the next set in our sequence is
$\Phi_1 = [0, \frac{1}{20}] \cup [\frac{19}{20},1]$. In general, for
$n = 1, \ldots$, we have that $\Phi_1$ is the union of $2^n$ disjoint
intervals of length

$$
\ell_n
    = \prod_{i=1}^n \frac{1}{10^i}
    = \frac{1}{10} \frac{1}{100} \ldots \frac{1}{10^n}
    = \frac{1}{10^{\frac{n(n+1)}{2}}}.
$$

To get to the next set in the sequence, we will remove from each
of the $2^n$ intervals of $\Phi_n$ the middle $\frac{10^n - 1}{10^n}$
the result of which is $2^{n+1}$ intervals, and we take $\Phi_{n+1}$
to be the union of these disjoint closed intervals. Next, we define
$\Phi$ to be

$$
\Phi = \bigcap_{n \in \mathbb{N}} \Phi_n.
$$

# The Proof!

Let $\alpha > 0$, and $\delta > 0$. For large enough $n$, we have that
the intervals of $\Phi_n$ have diameter less than $\delta$. Let
$\big\\{ I_j \big\\}_{j=1}^{2^n}$ be the intervals of $\Phi_n$. 
Anyway, so we need to examine the sum of their diameters raised by
$\alpha$:

$$
\sum_{i=1}^{2^n} d(I_j)
    = 2^n \ell_n^\alpha
    = (2^\frac{n}{\alpha} \ell_n)^\alpha
    = \Bigg(\frac{2^\frac{n}{\alpha}}{10^{\frac{n(n+1)}{2}}} \Bigg)^\alpha.
$$

Now, in taking the limit as $n \to \infty$, we have that this sum will
converge to 0, because the numerator does not grow nearly as fast as the
denominator, as the exponent goes quadratically on the bottom but linearly
on top. Thus, we have that $\mathcal{H}_{\alpha}^{\delta}(\Phi) = 0$ for any
$\delta > 0$, and so we then have that $\Phi$ has $\alpha$ dimensional
measure 0. Thus, $\Phi$has Hausdorff dimension 0.

I realized that I didn't show that $\Phi$ is uncountable, but I'm pretty
sure we can do that by putting a one to one correspondence between
$\\{ \Phi_n \\}_{n \in \mathcal{N}}$ and the sequence of sets in the 
construction of the Cantor set. Thus, $\Phi$ is an uncountable set with
Hausdorff dimension 0.


[fat-cantor]: https://en.wikipedia.org/wiki/Smith%E2%80%93Volterra%E2%80%93Cantor_set
