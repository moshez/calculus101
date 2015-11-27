Building the Real Numbers
=========================

At this point, with some understanding on how sequences and convergence work, we would like to take a step back and pay a debt --
 so far, we have been taking the real numbers' existence as an assumption. Now, we would like to build them.

We already have the rational numbers. We look at Cauchy sequences of rational numbers.
Let :math:`a_n` and :math:`b_n` be Cauchy sequences of rational numbers.
If :math:`b_n-a_n` converges to :math:`0`, we will call them equivalent.
It is straightforward to see that this is an equivalence relation.
We define addition and multiplication as :math:`a_n+b_n` and :math:`a_nb_n`.
It is straightforward to see that these definitions respect the equivalence relation.
We also note that if we identify a rational number, :math:`q` with the sequence :math:`q,q,...`,
then different rational numbers are not equivlanet distinct and a
sequence :math:`a_n` is equivalent to :math:`q` if and only if :math:`a_n` converges to :math:`q`.

We define the real numbers as the equivalence classes of Cauchy sequences of rational numbers.
In order to prove it is a field, we need to show that if :math:`a_n` is not equivalent to :math:`0`,
it has an inverse.
Not being equivalent to :math:`0` means there is an :math:`\epsilon` such that for every :math:`N` there is a an :math:`n>N` such that
:math:`|a_n|>\epsilon`.
Since :math:`a_n` is Cauchy, let `N` be such that :math:`|a_n-a_m|N`.
Since there is an :math:`n>N`, :math:`|a_n|>\epsilon`. Assume :math:`a_n>\epsilon`, then if :math:`m>N`, `a_m>=a_n-|a_n-a_m|>a_n-\epsilon/2>\epsilon/2`. In particular, if `m>N`, :math:`a_m\neq 0`. Let's define a sequence, :math:`b_n` to be :math:`1/a_n` if :math:`n>N` and :math:`0` otherwise. Then :math:`a_nb_n=1` if :math:`n>N`, and so :math:`a_nb_n` is equivalent to :math:`1` -- so :math:`b_n` is an inverse of :math:`a_n`.

We define :math:`a_n\leq b_n` if :math:`b_n-a_n` has a tail bounded from below by :math:`\epsilon` for every :math:`\epsilon`. The definition is subtle because we do want :math:`(1/n)\leq 0`. Checking that with this ordering relationship, the field becomes ordered is straightforward.

Let :math:`a_n` be a Cauchy sequence of rationals. Choose :math:`N` that corresponds to :math:`1` for this sequence. Then :math:`a_{N+1}` is a rational number, and if :math:`n>N`, :math:`a_n<a_{N+1}+1`. Since for every rational number there is a greater natural number :math:`M`, :math:`a_nN` and :math:`M>a_{N+1}`. Therefore, :math:`a_n\leq M` according to the definition above.

Now assume that :math:`m` is a natural number, and :math:`a` is a real number. There exists a natural number, :math:`n>ma` and so :math:`a0`. For every natual number :math:`n` there is a natural number :math:`m` such that :math:`m/2^n>b`. Since :math:`b` is an upper bound, that means that for every :math:`a` in :math:`A`, :math:`a\leq m/2^n`. For every :math:`n`, we take the smallest :math:`m` that satisfies the property (since any set of natural numbers has a minimal element). Now we note that if :math:`m/2^n` satisfies that property, then for :math:`n+1`, either `2m/2^{n+1}` satisfies the property, or `(2m-1)/2^{n+1}` because if `(2m-2)/2^{n+1}` is an upper bound, then so is :math:`(m-1)/2^{n+1}` in contradiction to minimality. In particular, if we define this sequence as :math:`c_n`, then :math:`|c_n-c_{n+1}|<1/2^{n+1}`. By induction, we can see that :math:`|c_n-c_m|n`. Therefore, :math:`c_n` is a Cauchy sequence of rationals. We can see that :math:`c_n>a` for every :math:`a` in :math:`A`, so :math:`c` is an upper bound for :math:`A`. We also note that :math:`c\leq c_n` for every :math:`n`, since :math:`c` is a decreasing sequence.

Is it a minimal upper bound? Assume :math:`d0`. In that case, :math:`1/(c-d)>0`. Let us take a natural number, :math:`N>1/(c-d)`, and so :math:`2^N>N>1/(c-d)`. Therefore, :math:`c-d>1/2^N`, or :math:`c>d+1/2^N`. But since :math:`d` is an upper bound, :math:`c-1/2^N\geq a` for all :math:`a` in :math:`A`. :math:`c_N-1/2^N\geq c-1/2^N\geq a`, and so for stage :math:`N`, :math:`m` was not minimally chosen, in contradiction. Therefore :math:`c` is a least upper bound.

For a general :math:`A`, let :math:`a_0` be a member in :math:`A`, and let :math:`A'` be the set all numbers expressible as `a-a_0+1` for :math:`a` in :math:`A`. if :math:`A` is bounded from above, so is :math:`A'`, and since :math:`1` is in :math:`A'`, :math:`A'` has a least upper bound :math:`c`. But if :math:`a-a_0+1\leq c`, :math:`a\leq c+a_0-1` and so :math:`c+a_0-1` is a least upper bound for :math:`A`.

This shows that rational Cauchy sequences under the right equivalence relation is a complete ordered field, and so a complete ordered field exists.
