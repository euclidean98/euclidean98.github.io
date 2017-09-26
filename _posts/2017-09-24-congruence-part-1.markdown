---
layout: post
title: "Congruence (Part I)"
date: 2017-09-24 10:53:01 -0400
categories: number-theory
---
Congruence is the language for modular arithmetic. It was introduced by Gauss in the 19th century in his book '_Disquisitiones Arithmeticae_'. In this blog post, I will provide a detailed explanation of the idea of congruences and some of the most important theorems about congruences.   

#### **Definition**
Let a,b be two integers. a is congruent to b **relative to** _m_, written: $$ a \equiv b \pmod m $$ if and only if $$ m \mid (a-b)$$.


**THEOREM 1**

$$Let\ a,b,m\in \mathbb{Z}\ and\ m \gt 0.\ a\equiv b \pmod m $$ if and only if the remainder of a divided by m equals the remainder of b divided by m. _**i.e.**,_

Let $$a=q_1\cdot m +r_1 \land b=q_2\cdot m+r_2$$ such that $$0\le r_1,r_2\lt m $$. Then,
the theorem claims that $$a\equiv b \pmod m\iff r_1 = r_2$$

**PROOF**
First, we assume $$r_1=r_2$$ to show that $$a\equiv b \pmod m$$.
Since $$r_1=r_2$$,

$$a-q_1\cdot m=b-q_2\cdot m\\i.e.\ a-b=q_1\cdot m-q_2\cdot m\\i.e.\ a-b=m(q_1-q_2)\\i.e., m\mid (a-b)$$

Conversely, we assume $$a\equiv b \pmod m$$ to show that $$r_1=r_2$$.
By the definition of congruence, we know the following:

$$m\mid(a-b)\\i.e.\ m\mid((q_1\cdot m+r_1)-(q_2\cdot m+r_2))\\
i.e.\ \exists k\in \mathbb{Z} :\ m\cdot k=(q_1\cdot m+r_1)-(q_2\cdot m+r_2)\\
i.e.\ m\cdot (k-q_1+q_2) = r_1-r_2\\
m\mid r_1-r_2. $$

$$Since -m\lt r_1-r_2 \lt m, r_1-r_2=0 \ \blacksquare$$
