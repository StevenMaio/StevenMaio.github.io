---
layout: post
title:  "First post"
date:   2019-03-27 21:01:34 -0400
categories: blog math
---

{% include mathjax_support.html %}

Hey, I'm Steven. I'm not complete sure about what I'm going to do with this
blog, but I need to practice writing, and this seems like a perfect
opportunity to do that.

```python
def hello():
    print("hello")
```

You can find my GitHub page [here][github]. I'm currently working through
Erwin Kreyszig's Introductory Functional Analysis.

To end this post, I'll leave the definition of a metric on a set $X$. We
define a metric $ d : X \times X \to R $ to be a function such that

1. $\forall x,y \in X, \; d(x, y) \ge 0$;
2. $d(x,y) = 0$ iff $x = y$;
3. $d(x,y) = d(y,x) \; \forall x,y \in x$; and
4. $d(x,y) \le d(x,z) + d(z,y) \; \forall x,y,z \in X$

This turns $X$ into a metric space, which is formally denoted as a tuple
$(X, d)$.

[github]: https://github.com/StevenMaio
