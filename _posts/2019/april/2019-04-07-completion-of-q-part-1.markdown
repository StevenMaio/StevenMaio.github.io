---
layout: post
mathjax: true
title:  "Constructing R from Q, Part 1: Fields, Sequences, bleh"
date:   2019-04-8 21:01:34
categories: blog math
---

What do I need for this post? I should provide an introduction to the problem.

1.  Definition of a field
2.  Assume that $ \mathbb{Q} $ is a field (I don't want to show this)
3.  Define sequences, and then Cauchy sequences

## Fields

Okay, so we're going to first start off with some of the defining properties of
$ \mathbb{Q} $. $ \mathbb{Q} $ is an example of what's called a field in
mathematics. A field $ F $ is a set equipped with two binary operations
$+, \cdot$; and it may be worth mentioning that these bear no relation to
addition or multiplication on the real numbers. These two operatoins come with
the following properties.

1. $(x + y) + z = x + (y + z)$ for any $x, y, z \in F$ )
2. $x + y = y + x$ ( for any $ x, y \in F$ )
3. There exists $ 0 \in F $ such that for any $x \in F$, $ 0 + x = x + 0 = x $
4. For any $ x \in F $ there exists $y \in F$ such that $x + y = y + x = 0$
5. $(xy)z = x(yz)$,  for all $ x,y,z \in F $
6. $xy = yx$ for any $ x,y \in F$
7. There exists $ 1 \in F$ such that for any $x \in F$ we have that $ 1x = x1 = x$
8. For any $ x \in F$ with $ x \ne 0$, there exists $ y \in F$ such that $xy = yx = 1$
9. For all $x,y,z \in F, \; x(y + z) = xy + xz$

From our experiences in a Math class, we already know that these properties
are also shared by $ \mathbb{R} $. Now, the goal of this blog is show how
$\mathbb{R}$ differs from $\mathbb{Q}$, and to give a more concrete property
other than the fact that $\pi$ is not a member of $\mathbb{Q}$.

## Sequences

Let's first start off with sequences. A sequence is a function
$a : \mathbb{N} \to X$, where by sake of convention and tradition, we denote
$a(n)$ by $a_n$. YOu will find, that often a sequence will be represented as 
$\{ a_n \}$ .For the purpose of this blog, $X$ will almost always be
$\mathbb{Q}$ (with some later exceptions which I won't bring up until then).

Now, we're going to consider the case when $X$ is a
[metric space](metric-space). We say that the sequence $\{ a_n \}$ in $X$
converges to $a \in X $ if for any $\epsilon > 0$, there exists
$N \in \mathbb{N}$, such that for any $n \ge N$, we have that

$$ d(a_n, a) < \epsilon $$

I think it's to safe that we're certainly on our way. But, it helps to look
at examples. We write this as

$$ \lim_{n \to \infty} a_n = a $$

And this is also denoted by $a_n \to a$.

### Example 1

For $n \in \mathbb{N}$, let $a_n = \frac{1}{n}$. If $k$ is some fixed positive
integer, then as $m$ gets larger, far larger than $k$ in fact, we have that
$\frac{1}{m}$ becomes smaller and smaller. From intuition and our experiences
in a math(s) class, we already formulated that 1 divided by $\infty$ is
essentially 0. While intuition isn't necessarily good enough, limits and
sequences turn out to be amazing tools at handling these statements which
feel right to us, but somehow escape reality and wording simultaneously.    # TODO: I dont' like this sentence

Now, we show that $a_n \to 0$. Let $\epsilon > 0$. From the Archimedean
property of the rational numbers, we know that there exists
$N \in \mathbb{N}$ for which $N \epsilon > 1$. Because $N$ is nonzero, we see
that we can divide through by $N$, and in doing so, we yield that

$$ \epsilon > \frac{1}{N} $$

Going back to our previous point, we have that if $n \ge N$, then
$\frac{1}{N} \ge \frac{1}{n}$. Thus, if $n \ge N$ we then have that


$$ d(a_n, 0) = |a_n - 0| = |a_n| = \frac{1}{n} \le \frac{1}{N} < \epsilon $$

Thus, we have that $a_n \to 0$.

Now, there is where !Q! and !R! begin to differ. As you may know, we can represent $\pi$

[metric-spaces]: https://en.wikipedia.org/wiki/Metric_space
