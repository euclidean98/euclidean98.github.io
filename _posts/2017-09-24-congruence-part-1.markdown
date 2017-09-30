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


<br>


**THEOREM 2** <br>(_Congruence is an equivalence relation._)

Let $$m\in \mathbb{Z} and\ m \gt 0.\\1.(Reflexivity)\ a\equiv a \pmod m \forall a \in \mathbb{Z}.\\
    2.(Commutativity)\ a\equiv b \pmod m \iff\ b\equiv a \pmod m\\ 3.(Transitivity)\ a\equiv b \pmod m \land b\equiv c\pmod m
    \Rightarrow a\equiv c \pmod m $$

**PROOF**

1.$$\ a\equiv a \pmod m \iff m\mid a-a\\i.e.\ m\mid 0, which\ is\ true. \square$$  
2.$$\ a\equiv b \pmod m \iff m\mid a-b\iff \exists k \in \mathbb{Z}:a-b=m\cdot k\\
So,\ b-a = -m\cdot k\\i.e.\ m\mid (b-a). \square$$  
3.$$\ Since,\ a\equiv b \pmod m,\ m\mid (a-b).\ Also,\ b\equiv c\pmod m,\ m\mid (b-c).$$
$$\text{So, m divides all combinations of (a-b) and (b-c). In particular, }m\mid {(a-b)+(b-c)}
\\i.e.\ m\mid (a-c) \ \blacksquare$$

<br>

**THEOREM 3**

$$Let\ a,b,c,d,m\in \mathbb{Z}\ and\ m \gt 0.\\ If\ a\equiv b\pmod m \land \ c\equiv d\pmod m\  then,\\ a+c\equiv b+d\pmod m\ \land a\cdot c\equiv b\cdot d\pmod m.$$

**PROOF**

$$a\equiv b\pmod m \to m\mid (a-b) \\ c\equiv d\pmod m \to m\mid (c-d)\\
So,\ m\ divides\ all\ combinations\ of\ (a-b)\ and\ (c-d).\\In\ particular,\\
m\mid (a-b)+(c-d)\\i.e.\ m\mid (a+c)-(b+d)\\i.e.\ a+c\equiv b+d\pmod m\\Similarly,\\
m\mid c\cdot(a-b)+b\cdot(c-d)\\i.e.\ m\mid ac - bd\\i.e. a\cdot c \equiv b\cdot d \pmod m$$

**Corollaries of Theorem 3**

_Corollary #1_ <br>

$$If\ a\equiv b \pmod m,\ for\ \forall n\in \mathbb{Z}\ a^n\equiv b^n\pmod m$$ (From repeated application of part 2 of theorem 3)

_Corollary #2_ <br>

$$Let\ p(x)=c_n\cdot x^n + c_n-1\cdot x^n-1 +\ ...\ + c_1\cdot x + c_0\ be\ a\ polynomial\ and\ a,b \in \mathbb{Z}.\\If\ a\equiv b \pmod m\ ,then\ p(a)\equiv p(b) \pmod m.$$
**Proof**
$$\\\\From\ corollary\ 1,\ for\ each\ power,\ let\ k,\ of\ x\ in\ p(x),\ a^k\equiv b^k\pmod m.\\ So, c_k\cdot a^k \equiv c_k\cdot b^k \pmod m,\ from\ part\ 2\ of\ theorem\ 3.\\Adding\ all\ congruences\ obtained\ by\ taking\ all\ powers\ in\ the\ polynomial\ p(x),\\ from\ part\ 1\ of\ theorem\ 3,\ p(a)\equiv p(b) \pmod m. \square$$
