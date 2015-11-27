Completeness
============

We already know that every bounded monotonic sequence converges. This is powerful -- we know it converges, even though we cannot, necessarily point to the limit. Clearly, however, this is not necessary for convergence -- we have already seen sequences which are not monotonic converge.

If we try to find a universal criterion for convergence, we need to start with things of which we are sure.
We know, for example, we need to limit ourselves to tail properties.
We also know that for any given :math:`\epsilon`, from some point on :math:`|a_n-a|<\epsilon`.
However, that mentions the limit, and we would like to avoid that.
One way of doing it is noting that in that tail :math:`|a_n-a_m|<2\epsilon`, for any :math:`n,m`.
As we have already seen in our proof for convergence of addition, things like :math:`2\epsilon` are not interesting:
after all, if we had taken the tail corresponding to `\epsilon/2`, we would have gotten :math:`|a_n-a_m|<\epsilon`.

A sequence with the property that for every :math:`\epsilon`, there is an :math:`N` such that for all
:math:`n,m > N`, :math:`|a_n - a_m| < \epsilon` is called a Cauchy sequence.
The discussion above shows that every converging sequence is a Cauchy sequence.

We know that in the rational numbers, not every Cauchy sequence converges:
for example, the sequences we defined as :math:`a_n` and :math:`b_n` in the chapter about irrational numbers
are Cauchy, but do not converge in the rational numbers.
Is it possible for sequences of real numbers to be Cauchy and not to converge in the real numbers?
It turns out the answer is negative.

Assume :math:`a_n` is Cauchy. We remember that despite not looking it, being bounded is a tail property.
If we take `\epsilon=1`, we have that for some :math:`N`, if :math:`n>N` then :math:`|a_n-a_0|<1`, or :math:`a_0-1<a_n<a_0+1`.
Since the sequence has a bounded tail, it is bounded.
Therefore, it has a converging subsequence. Call the subsequence :math:`a_{n_k}`.
Now let :math:`\epsilon > 0`.
Find :math:`N` from the Cauchy property such that if :math:`n,m>N` :math:`|a_n - a_m|<\epsilon/2`.
Find :math:`M` from the convergence of the subsequence such that if :math:`k>M`, :math:`|a_{n_k} - a|<\epsilon/2`.
Now let :math:`O` be the biggest of :math:`N` and :math:`M`. Then if :math:`n>O` then :math:`n_{O+1} \geq O+1 > O \geq N`,
so :math:`|a_n - a_{n_{O+1}}| < \epsilon/2` and :math:`|a_{n_{O+1}} - a|<\epsilon/2`.
Adding the inequalities, and using the triangle inequality, we get that if :math:`n>O` then
:math:`|a_n - a|=|a_n - a_{n_{O+1}} + a_{n_{O+1}} - a| \leq |a_n - a_{n_{O+1}}| + |a_{n+{O+1}} - a| < \epsilon/2 + \epsilon/2 = \epsilon`.
Therefore, :math:`a_n` converges to :math:`a`.

This gives us a general machine to produce limits: define a sequence, show it is Cauchy, and then take its limit.

As an example of how to use the machine, we define here the decimal expansion.

Let :math:`d_n` be a sequence of integers between :math:`0` and :math:`9`.
We will define a sequence by induction: :math:`a_0=0`, :math:`a_{n+1}=a_n+d_n/10^n`.
In order to prove it is Cauchy, we will first note :math:`|a_{n+1}-a_n|\leq 9/10^n`.
We will prove by induction :math:`|a_{n+k}-a_n|\leq 9/10^n[1-1/10^k]/[1-1/10]`.
The case for :math:`0` is trivial, since the difference between an element and itself is :math:`0`.
Assume it holds for :math:`k`, and now
:math:`|a_{n+k+1}-a_n|\leq|a_{n+k+1}-a_{n+k}|+|a_{n+k}-a_n|\leq 9/10^{n+k}+9/10^n[1-1/10^k]/[1-1/10]=9/10^n[1/10^k+[1-1/10^k]/[1-1/10]=9/10^n[1-1/10^{k+1}]/[1-1/10]`.

We also note that :math:`9/10^n\leq 9/n`. Thus, if :math:`N>2*9/\epsilon`, :math:`|a_{N+k}-a_N`<\epsilon/2`, and thus
:math:`|a_{N+k}-a_{N+l}|<\epsilon`, then
:math:`n=N+k,m=N+l` for some :math:`k`, we see that the sequence we defined is Cauchy.
We call its limit :math:`0.d_0d_1...` the "decimal number" corresponding to the sequence of digits.
Note that we have not used any special properties of :math:`10` here, so that we can have expansions by any base.

(A proper treatment of decimal expansions would show that every real number between :math:`0` and :math:`1` has a decimal expansion,
and would analyze the circumstances under which it is unique, but this is beyond the scope of showing the Cauchy machinery
in use.)
